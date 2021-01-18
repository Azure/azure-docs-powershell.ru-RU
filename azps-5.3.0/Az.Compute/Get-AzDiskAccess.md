---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519642"
---
# <span data-ttu-id="84a3c-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="84a3c-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="84a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="84a3c-103">Свойства дискового доступа</span><span class="sxs-lookup"><span data-stu-id="84a3c-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="84a3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84a3c-104">SYNTAX</span></span>

### <span data-ttu-id="84a3c-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84a3c-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84a3c-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a3c-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84a3c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84a3c-107">DESCRIPTION</span></span>
<span data-ttu-id="84a3c-108">Для получения свойств дискового доступа к диску возвращается cmdlet **Get-AzDiskAccess.**</span><span class="sxs-lookup"><span data-stu-id="84a3c-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="84a3c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84a3c-109">EXAMPLES</span></span>

### <span data-ttu-id="84a3c-110">Пример 1. Использование набора параметров по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84a3c-110">Example 1: Using Default Parameter Set</span></span> 
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

<span data-ttu-id="84a3c-111">Эта команда получает свойства ресурса Диска Access с именем "ДискAccess01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="84a3c-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="84a3c-112">Пример 2. Get-AzDiskAccess по группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="84a3c-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
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

<span data-ttu-id="84a3c-113">Эта команда получает свойства всех дискового доступа в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="84a3c-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="84a3c-114">Пример 3. Получение всего дискового доступа</span><span class="sxs-lookup"><span data-stu-id="84a3c-114">Example 3: Getting all Disk Access</span></span>
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

<span data-ttu-id="84a3c-115">Эта команда получает свойства всех дискового доступа в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="84a3c-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="84a3c-116">Пример 4. Доступ ко всему диску с помощью поддиавных символов</span><span class="sxs-lookup"><span data-stu-id="84a3c-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
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

<span data-ttu-id="84a3c-117">Эта команда получает свойства всех дискового доступа под именем подписки, начиная с "DiskAccessMicrosoft".</span><span class="sxs-lookup"><span data-stu-id="84a3c-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="84a3c-118">Пример 5. Доступ к диску с помощью ResourceId.</span><span class="sxs-lookup"><span data-stu-id="84a3c-118">Example 5: Get Disk Access using ResourceId.</span></span>
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

<span data-ttu-id="84a3c-119">Эта команда получает свойства дискового доступа с заданным объектом ResourceId.</span><span class="sxs-lookup"><span data-stu-id="84a3c-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="84a3c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84a3c-120">PARAMETERS</span></span>

### <span data-ttu-id="84a3c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a3c-121">-DefaultProfile</span></span>
<span data-ttu-id="84a3c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84a3c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a3c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="84a3c-123">-Name</span></span>
<span data-ttu-id="84a3c-124">Указывает имя дискового доступа.</span><span class="sxs-lookup"><span data-stu-id="84a3c-124">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="84a3c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a3c-125">-ResourceGroupName</span></span>
<span data-ttu-id="84a3c-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84a3c-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="84a3c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84a3c-127">-ResourceId</span></span>
<span data-ttu-id="84a3c-128">ИД ресурса для доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="84a3c-128">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="84a3c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a3c-129">CommonParameters</span></span>
<span data-ttu-id="84a3c-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a3c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a3c-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84a3c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a3c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84a3c-132">INPUTS</span></span>

### <span data-ttu-id="84a3c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="84a3c-133">System.String</span></span>

## <span data-ttu-id="84a3c-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84a3c-134">OUTPUTS</span></span>

### <span data-ttu-id="84a3c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIskAccess</span><span class="sxs-lookup"><span data-stu-id="84a3c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="84a3c-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84a3c-136">NOTES</span></span>

## <span data-ttu-id="84a3c-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84a3c-137">RELATED LINKS</span></span>
