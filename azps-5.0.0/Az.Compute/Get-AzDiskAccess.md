---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316696"
---
# <span data-ttu-id="66e22-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="66e22-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="66e22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66e22-102">SYNOPSIS</span></span>
<span data-ttu-id="66e22-103">Возвращает свойства доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="66e22-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="66e22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66e22-104">SYNTAX</span></span>

### <span data-ttu-id="66e22-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66e22-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66e22-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="66e22-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66e22-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66e22-107">DESCRIPTION</span></span>
<span data-ttu-id="66e22-108">Командлет **Get-AzDiskAccess** получает свойства доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="66e22-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="66e22-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66e22-109">EXAMPLES</span></span>

### <span data-ttu-id="66e22-110">Пример 1: использование параметра по умолчанию</span><span class="sxs-lookup"><span data-stu-id="66e22-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="66e22-111">Эта команда получает свойства ресурса доступа к диску с именем "DiskAccess01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="66e22-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="66e22-112">Пример 2: Get-AzDiskAccess по группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="66e22-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="66e22-113">Эта команда получает свойства всех обращений к дискам в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="66e22-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="66e22-114">Пример 3: получение доступа ко всем дискам</span><span class="sxs-lookup"><span data-stu-id="66e22-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="66e22-115">Эта команда получает свойства всех обращений к дискам в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="66e22-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="66e22-116">Пример 4: получение доступа ко всем дискам с помощью подстановочных знаков</span><span class="sxs-lookup"><span data-stu-id="66e22-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="66e22-117">Эта команда получает свойства всех обращений к дискам под именем подписки, начинающейся с "DiskAccessMicrosoft".</span><span class="sxs-lookup"><span data-stu-id="66e22-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="66e22-118">Пример 5: получение доступа к диску с помощью ResourceId.</span><span class="sxs-lookup"><span data-stu-id="66e22-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="66e22-119">Эта команда получает свойства доступа к диску с данным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="66e22-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="66e22-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66e22-120">PARAMETERS</span></span>

### <span data-ttu-id="66e22-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e22-121">-DefaultProfile</span></span>
<span data-ttu-id="66e22-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66e22-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66e22-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66e22-123">-Name</span></span>
<span data-ttu-id="66e22-124">Указывает имя доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="66e22-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="66e22-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e22-125">-ResourceGroupName</span></span>
<span data-ttu-id="66e22-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66e22-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="66e22-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66e22-127">-ResourceId</span></span>
<span data-ttu-id="66e22-128">Идентификатор ресурса для доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="66e22-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66e22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e22-129">CommonParameters</span></span>
<span data-ttu-id="66e22-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66e22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e22-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66e22-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e22-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66e22-132">INPUTS</span></span>

### <span data-ttu-id="66e22-133">System. String</span><span class="sxs-lookup"><span data-stu-id="66e22-133">System.String</span></span>

## <span data-ttu-id="66e22-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66e22-134">OUTPUTS</span></span>

### <span data-ttu-id="66e22-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="66e22-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="66e22-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="66e22-136">NOTES</span></span>

## <span data-ttu-id="66e22-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66e22-137">RELATED LINKS</span></span>
