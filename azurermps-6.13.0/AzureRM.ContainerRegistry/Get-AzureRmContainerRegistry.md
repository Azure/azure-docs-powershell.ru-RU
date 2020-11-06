---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: 3d9580549308c17c92037b3e31a337f11bbe6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556748"
---
# <span data-ttu-id="36e08-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36e08-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="36e08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36e08-102">SYNOPSIS</span></span>
<span data-ttu-id="36e08-103">Получает реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="36e08-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36e08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36e08-104">SYNTAX</span></span>

### <span data-ttu-id="36e08-105">ListRegistriesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36e08-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36e08-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36e08-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36e08-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36e08-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36e08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36e08-108">DESCRIPTION</span></span>
<span data-ttu-id="36e08-109">Командлет Get-AzureRmContainerRegistry получает указанный реестр контейнера или все регистры контейнеров в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="36e08-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="36e08-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36e08-110">EXAMPLES</span></span>

### <span data-ttu-id="36e08-111">Пример 1: получение реестра в указанном контейнере</span><span class="sxs-lookup"><span data-stu-id="36e08-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="36e08-112">Эта команда получает указанный реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="36e08-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="36e08-113">Пример 2: получение всех реестров контейнеров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="36e08-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="36e08-114">Эта команда возвращает все реестры контейнеров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36e08-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="36e08-115">Пример 3: получение всех реестров контейнеров в подписке</span><span class="sxs-lookup"><span data-stu-id="36e08-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="36e08-116">Эта команда получает все реестры контейнеров в подписке.</span><span class="sxs-lookup"><span data-stu-id="36e08-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="36e08-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36e08-117">PARAMETERS</span></span>

### <span data-ttu-id="36e08-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e08-118">-DefaultProfile</span></span>
<span data-ttu-id="36e08-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36e08-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36e08-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="36e08-120">-IncludeDetail</span></span>
<span data-ttu-id="36e08-121">Показать дополнительные сведения о реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="36e08-121">Show more details about the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e08-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36e08-122">-Name</span></span>
<span data-ttu-id="36e08-123">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="36e08-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e08-124">-ResourceGroupName</span></span>
<span data-ttu-id="36e08-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36e08-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e08-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36e08-126">-ResourceId</span></span>
<span data-ttu-id="36e08-127">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="36e08-127">The container registry resource id</span></span>

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

### <span data-ttu-id="36e08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e08-128">CommonParameters</span></span>
<span data-ttu-id="36e08-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36e08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e08-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e08-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e08-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36e08-131">INPUTS</span></span>

### <span data-ttu-id="36e08-132">System. String</span><span class="sxs-lookup"><span data-stu-id="36e08-132">System.String</span></span>

## <span data-ttu-id="36e08-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36e08-133">OUTPUTS</span></span>

### <span data-ttu-id="36e08-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36e08-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="36e08-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="36e08-135">NOTES</span></span>

## <span data-ttu-id="36e08-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36e08-136">RELATED LINKS</span></span>

[<span data-ttu-id="36e08-137">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36e08-137">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="36e08-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36e08-138">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="36e08-139">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="36e08-139">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

