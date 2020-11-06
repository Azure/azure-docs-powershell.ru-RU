---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556747"
---
# <span data-ttu-id="c59e7-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c59e7-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="c59e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c59e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c59e7-103">Получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="c59e7-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c59e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c59e7-104">SYNTAX</span></span>

### <span data-ttu-id="c59e7-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c59e7-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c59e7-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c59e7-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c59e7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c59e7-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c59e7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c59e7-108">DESCRIPTION</span></span>
<span data-ttu-id="c59e7-109">Командлет Get-AzureRmContainerRegistryCredential получает учетные данные для входа в реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="c59e7-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="c59e7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c59e7-110">EXAMPLES</span></span>

### <span data-ttu-id="c59e7-111">Пример 1: получение учетных данных для входа в реестр контейнера</span><span class="sxs-lookup"><span data-stu-id="c59e7-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="c59e7-112">Эта команда получает учетные данные для входа в указанный контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="c59e7-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="c59e7-113">Чтобы \` получить учетные данные для входа, необходимо включить администратора в реестре MyRegistry \` .</span><span class="sxs-lookup"><span data-stu-id="c59e7-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="c59e7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c59e7-114">PARAMETERS</span></span>

### <span data-ttu-id="c59e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59e7-115">-DefaultProfile</span></span>
<span data-ttu-id="c59e7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c59e7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c59e7-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c59e7-117">-Name</span></span>
<span data-ttu-id="c59e7-118">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="c59e7-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="c59e7-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="c59e7-119">-Registry</span></span>
<span data-ttu-id="c59e7-120">Объект реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="c59e7-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="c59e7-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c59e7-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c59e7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c59e7-123">-ResourceId</span></span>
<span data-ttu-id="c59e7-124">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="c59e7-124">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59e7-125">CommonParameters</span></span>
<span data-ttu-id="c59e7-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c59e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59e7-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c59e7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59e7-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c59e7-128">INPUTS</span></span>

### <span data-ttu-id="c59e7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c59e7-129">System.String</span></span>

## <span data-ttu-id="c59e7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c59e7-130">OUTPUTS</span></span>

### <span data-ttu-id="c59e7-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c59e7-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="c59e7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c59e7-132">NOTES</span></span>

## <span data-ttu-id="c59e7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c59e7-133">RELATED LINKS</span></span>

[<span data-ttu-id="c59e7-134">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c59e7-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="c59e7-135">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c59e7-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="c59e7-136">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c59e7-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

