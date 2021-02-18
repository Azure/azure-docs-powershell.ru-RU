---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227980"
---
# <span data-ttu-id="e4413-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4413-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="e4413-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4413-102">SYNOPSIS</span></span>
<span data-ttu-id="e4413-103">Получает группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="e4413-103">Gets an application security group.</span></span>

## <span data-ttu-id="e4413-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4413-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4413-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4413-105">DESCRIPTION</span></span>
<span data-ttu-id="e4413-106">Для получения группы безопасности приложений возвращается cmdlet **Get-AzApplicationSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="e4413-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="e4413-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4413-107">EXAMPLES</span></span>

### <span data-ttu-id="e4413-108">Пример 1. Извлечение всех групп безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="e4413-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="e4413-109">Вышеуказанная команда возвращает все группы безопасности приложений в подписке.</span><span class="sxs-lookup"><span data-stu-id="e4413-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="e4413-110">Пример 2. Извлечение групп безопасности приложений в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4413-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="e4413-111">Вышеуказанная команда возвращает все группы безопасности приложений, которые относятся к группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4413-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e4413-112">Пример 3. Получение определенной группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="e4413-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="e4413-113">Вышеуказанная команда возвращает группу безопасности приложений MyApplicationSecurityGroup в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4413-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e4413-114">Пример 4. Извлечение групп безопасности приложений с помощью фильтрации.</span><span class="sxs-lookup"><span data-stu-id="e4413-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="e4413-115">Вышеуказанная команда возвращает все группы безопасности приложений, которые начинаются с "MyApplicationSecurityGroup".</span><span class="sxs-lookup"><span data-stu-id="e4413-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="e4413-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4413-116">PARAMETERS</span></span>

### <span data-ttu-id="e4413-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4413-117">-DefaultProfile</span></span>
<span data-ttu-id="e4413-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4413-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4413-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e4413-119">-Name</span></span>
<span data-ttu-id="e4413-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e4413-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e4413-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4413-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4413-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4413-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e4413-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4413-123">CommonParameters</span></span>
<span data-ttu-id="e4413-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4413-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4413-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4413-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4413-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4413-126">INPUTS</span></span>

### <span data-ttu-id="e4413-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e4413-127">System.String</span></span>

## <span data-ttu-id="e4413-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4413-128">OUTPUTS</span></span>

### <span data-ttu-id="e4413-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4413-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="e4413-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4413-130">NOTES</span></span>

## <span data-ttu-id="e4413-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4413-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4413-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4413-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="e4413-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e4413-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="e4413-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e4413-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e4413-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e4413-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
