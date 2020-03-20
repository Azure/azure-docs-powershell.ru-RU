---
title: Использование Azure PowerShell в Docker
description: Использование предустановки Azure PowerShell в образе Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402686"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="ce0e6-103">Использование Azure PowerShell в Docker</span><span class="sxs-lookup"><span data-stu-id="ce0e6-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="ce0e6-104">Мы публикуем образы Docker с предустановкой Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="ce0e6-105">В этой статье показано, как приступить к работе с Azure PowerShell в контейнере Docker.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="ce0e6-106">Поиск доступных образов</span><span class="sxs-lookup"><span data-stu-id="ce0e6-106">Finding available images</span></span>

<span data-ttu-id="ce0e6-107">Для выпущенных образов требуется Docker 17.05 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="ce0e6-108">Также предполагается, что Docker можно запускать без `sudo` или прав локального администратора.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="ce0e6-109">Чтобы правильно установить `docker`, следуйте официальным [инструкциям][install] Docker.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="ce0e6-110">Выпущенные контейнеры создаются на основе официальных контейнеров PowerShell, к которым затем в качестве определенного уровня добавляется модуль Az.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="ce0e6-111">Последний стабильный образ включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="ce0e6-111">The latest stable image includes:</span></span>

- <span data-ttu-id="ce0e6-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="ce0e6-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="ce0e6-113">PowerShell версии 6.2.4</span><span class="sxs-lookup"><span data-stu-id="ce0e6-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="ce0e6-114">Актуальный модуль Az Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ce0e6-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="ce0e6-115">См. [полный список доступных образов Docker][az image].</span><span class="sxs-lookup"><span data-stu-id="ce0e6-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="ce0e6-116">Использование Azure PowerShell в контейнере</span><span class="sxs-lookup"><span data-stu-id="ce0e6-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="ce0e6-117">Ниже представлены команды Docker, необходимые для скачивания образа и запуска интерактивного сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="ce0e6-118">Скачайте последнюю версию образа azure-powershell.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="ce0e6-119">Запустите контейнер azure-powershell в интерактивном режиме:</span><span class="sxs-lookup"><span data-stu-id="ce0e6-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="ce0e6-120">Запуск контейнера azure-powershell в интерактивном режиме с использованием проверки подлинности узла</span><span class="sxs-lookup"><span data-stu-id="ce0e6-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="ce0e6-121">Если в системе с Docker есть установка Azure PowerShell, возможно, доступны кэшированные учетные данные Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="ce0e6-122">Эти учетные данные можно использовать в сеансе PowerShell, выполняющемся в контейнере Docker.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="ce0e6-123">По умолчанию кэшированные учетные данные находятся в каталоге `$HOME/.Azure` на узле.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="ce0e6-124">Служба Docker должна иметь доступ к этому расположению для получения доступа к учетным данным.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="ce0e6-125">Следующая команда запускает контейнер с подключенным кэшем учетных данных, а также интерактивный сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="ce0e6-126">Удаление ненужного образа</span><span class="sxs-lookup"><span data-stu-id="ce0e6-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="ce0e6-127">Приведенная ниже команда служит для удаления контейнера Docker, если он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="ce0e6-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="ce0e6-128">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="ce0e6-128">Next steps</span></span>

<span data-ttu-id="ce0e6-129">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="ce0e6-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell