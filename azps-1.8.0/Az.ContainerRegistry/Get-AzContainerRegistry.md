---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: d0ba9315efd61657359bb45883b83cb2bae0095a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731186"
---
# <span data-ttu-id="5b16e-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5b16e-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="5b16e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b16e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b16e-103">Получает реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="5b16e-103">Gets a container registry.</span></span>

## <span data-ttu-id="5b16e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b16e-104">SYNTAX</span></span>

### <span data-ttu-id="5b16e-105">ListRegistriesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b16e-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b16e-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b16e-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b16e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b16e-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b16e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b16e-108">DESCRIPTION</span></span>
<span data-ttu-id="5b16e-109">Командлет Get-AzContainerRegistry получает указанный реестр контейнера или все регистры контейнеров в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="5b16e-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="5b16e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b16e-110">EXAMPLES</span></span>

### <span data-ttu-id="5b16e-111">Пример 1: получение реестра в указанном контейнере</span><span class="sxs-lookup"><span data-stu-id="5b16e-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="5b16e-112">Эта команда получает указанный реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="5b16e-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="5b16e-113">Пример 2: получение всех реестров контейнеров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5b16e-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

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

<span data-ttu-id="5b16e-114">Эта команда возвращает все реестры контейнеров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b16e-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="5b16e-115">Пример 3: получение всех реестров контейнеров в подписке</span><span class="sxs-lookup"><span data-stu-id="5b16e-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

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

<span data-ttu-id="5b16e-116">Эта команда получает все реестры контейнеров в подписке.</span><span class="sxs-lookup"><span data-stu-id="5b16e-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="5b16e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b16e-117">PARAMETERS</span></span>

### <span data-ttu-id="5b16e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b16e-118">-DefaultProfile</span></span>
<span data-ttu-id="5b16e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5b16e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="5b16e-120">-IncludeDetail</span></span>
<span data-ttu-id="5b16e-121">Показать дополнительные сведения о реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="5b16e-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="5b16e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b16e-122">-Name</span></span>
<span data-ttu-id="5b16e-123">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="5b16e-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="5b16e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b16e-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b16e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b16e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="5b16e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b16e-126">-ResourceId</span></span>
<span data-ttu-id="5b16e-127">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="5b16e-127">The container registry resource id</span></span>

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

### <span data-ttu-id="5b16e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b16e-128">CommonParameters</span></span>
<span data-ttu-id="5b16e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b16e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b16e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b16e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b16e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b16e-131">INPUTS</span></span>

### <span data-ttu-id="5b16e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5b16e-132">System.String</span></span>

## <span data-ttu-id="5b16e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b16e-133">OUTPUTS</span></span>

### <span data-ttu-id="5b16e-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5b16e-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="5b16e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b16e-135">NOTES</span></span>

## <span data-ttu-id="5b16e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b16e-136">RELATED LINKS</span></span>

[<span data-ttu-id="5b16e-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5b16e-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="5b16e-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5b16e-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="5b16e-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5b16e-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

