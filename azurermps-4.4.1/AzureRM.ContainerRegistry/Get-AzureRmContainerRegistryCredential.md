---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566286"
---
# <span data-ttu-id="627f0-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="627f0-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="627f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="627f0-102">SYNOPSIS</span></span>
<span data-ttu-id="627f0-103">Получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="627f0-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="627f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="627f0-104">SYNTAX</span></span>

### <span data-ttu-id="627f0-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="627f0-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627f0-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="627f0-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="627f0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="627f0-107">DESCRIPTION</span></span>
<span data-ttu-id="627f0-108">Командлет **Get-AzureRmContainerRegistryCredential** получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="627f0-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="627f0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="627f0-109">EXAMPLES</span></span>

### <span data-ttu-id="627f0-110">Пример 1: получение учетных данных для входа в реестр контейнера</span><span class="sxs-lookup"><span data-stu-id="627f0-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="627f0-111">Эта команда получает учетные данные для входа в указанный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="627f0-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="627f0-112">Чтобы получить учетные данные для входа, пользователю администратора необходимо включить параметр Container в реестре `MyRegistry` .</span><span class="sxs-lookup"><span data-stu-id="627f0-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="627f0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="627f0-113">PARAMETERS</span></span>

### <span data-ttu-id="627f0-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="627f0-114">-Name</span></span>
<span data-ttu-id="627f0-115">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="627f0-115">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627f0-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="627f0-116">-Registry</span></span>
<span data-ttu-id="627f0-117">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="627f0-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="627f0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="627f0-118">-ResourceGroupName</span></span>
<span data-ttu-id="627f0-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="627f0-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627f0-120">-DefaultProfile</span></span>
<span data-ttu-id="627f0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="627f0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627f0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627f0-122">CommonParameters</span></span>
<span data-ttu-id="627f0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="627f0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627f0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="627f0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627f0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="627f0-125">INPUTS</span></span>

### <span data-ttu-id="627f0-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="627f0-126">PSContainerRegistry</span></span>
<span data-ttu-id="627f0-127">Параметр "Registry" принимает значение типа "PSContainerRegistry" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="627f0-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="627f0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="627f0-128">OUTPUTS</span></span>

### <span data-ttu-id="627f0-129">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="627f0-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="627f0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="627f0-130">NOTES</span></span>

## <span data-ttu-id="627f0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="627f0-131">RELATED LINKS</span></span>

[<span data-ttu-id="627f0-132">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="627f0-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="627f0-133">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="627f0-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="627f0-134">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="627f0-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

