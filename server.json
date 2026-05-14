const http = require("http");
const { Server } = require("socket.io");

const app = express();
const server = http.createServer(app);
const io = new Server(server, {
  cors: { origin: "*" }
  });

  app.use(express.static("public"));

  io.on("connection", (socket) => {

    socket.on("join-room", (room) => {
        socket.join(room);
          });

            socket.on("signal", ({ room, data }) => {
                socket.to(room).emit("signal", data);
                  });

                  });

                  server.listen(process.env.PORT || 3000, () => {
                    console.log("Servidor listo");
                    });