---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: dc1b35831de68ad31877be05610d1b075b27452f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568608"
---
# <span data-ttu-id="69344-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69344-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="69344-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69344-102">SYNOPSIS</span></span>
<span data-ttu-id="69344-103">Получает реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="69344-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69344-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69344-104">SYNTAX</span></span>

### <span data-ttu-id="69344-105">ListRegistriesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69344-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69344-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69344-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69344-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69344-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69344-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69344-108">DESCRIPTION</span></span>
<span data-ttu-id="69344-109">Командлет Get-AzureRmContainerRegistry получает указанный реестр контейнера или все регистры контейнеров в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="69344-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="69344-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69344-110">EXAMPLES</span></span>

### <span data-ttu-id="69344-111">Пример 1: получение реестра в указанном контейнере</span><span class="sxs-lookup"><span data-stu-id="69344-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="69344-112">Эта команда получает указанный реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="69344-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="69344-113">Пример 2: получение всех реестров контейнеров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="69344-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="69344-114">Эта команда возвращает все реестры контейнеров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69344-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="69344-115">Пример 3: получение всех реестров контейнеров в подписке</span><span class="sxs-lookup"><span data-stu-id="69344-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="69344-116">Эта команда получает все реестры контейнеров в подписке.</span><span class="sxs-lookup"><span data-stu-id="69344-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="69344-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69344-117">PARAMETERS</span></span>

### <span data-ttu-id="69344-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="69344-118">-Name</span></span>
<span data-ttu-id="69344-119">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="69344-119">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69344-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69344-120">-ResourceGroupName</span></span>
<span data-ttu-id="69344-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="69344-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListRegistriesParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69344-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69344-122">-DefaultProfile</span></span>
<span data-ttu-id="69344-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="69344-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69344-124">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="69344-124">-IncludeDetail</span></span>
<span data-ttu-id="69344-125">Показать дополнительные сведения о реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="69344-125">Show more details about the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69344-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69344-126">-ResourceId</span></span>
<span data-ttu-id="69344-127">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="69344-127">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69344-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69344-128">CommonParameters</span></span>
<span data-ttu-id="69344-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69344-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69344-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69344-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69344-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69344-131">INPUTS</span></span>

### <span data-ttu-id="69344-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="69344-132">None</span></span>
<span data-ttu-id="69344-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="69344-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69344-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69344-134">OUTPUTS</span></span>

### <span data-ttu-id="69344-135">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69344-135">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="69344-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="69344-136">NOTES</span></span>

## <span data-ttu-id="69344-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69344-137">RELATED LINKS</span></span>

[<span data-ttu-id="69344-138">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69344-138">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="69344-139">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69344-139">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="69344-140">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69344-140">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

