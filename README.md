# my-linktree
import React from "react";
import "tailwindcss/tailwind.css";

const links = [
  { name: "Google's 5-Day Gen AI Course", url: "#" },
  { name: "Ray-Ban Meta Smart Glasses", url: "#" },
  { name: "1:1 Mentorship with Maryam", url: "#" },
  { name: "Subscribe to AI JeeBee Newsletter", url: "#" },
  { name: "BoldVoice", url: "#" },
];

export default function LinktreePage() {
  return (
    <div className="min-h-screen flex flex-col items-center justify-center bg-gradient-to-r from-blue-500 to-orange-500 p-6">
      <div className="relative w-40 h-40 rounded-full overflow-hidden border-4 border-white shadow-lg">
        <img
          src="https://via.placeholder.com/150"
          alt="Profile"
          className="w-full h-full object-cover"
        />
      </div>
      <h1 className="text-white text-2xl font-bold mt-4">@Your_Username</h1>
      <div className="w-full max-w-md mt-6">
        {links.map((link, index) => (
          <a
            key={index}
            href={link.url}
            target="_blank"
            rel="noopener noreferrer"
            className="block w-full bg-black text-white text-center py-3 my-2 rounded-lg shadow-md hover:bg-gray-800 transition duration-300"
          >
            {link.name}
          </a>
        ))}
      </div>
    </div>
  );
}
