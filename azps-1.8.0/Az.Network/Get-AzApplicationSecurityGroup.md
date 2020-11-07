---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: 58bae669af1fb9a06f4caa95070225f12d1a78aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730621"
---
# <span data-ttu-id="4c92a-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4c92a-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="4c92a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c92a-102">SYNOPSIS</span></span>
<span data-ttu-id="4c92a-103">Получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="4c92a-103">Gets an application security group.</span></span>

## <span data-ttu-id="4c92a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c92a-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c92a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c92a-105">DESCRIPTION</span></span>
<span data-ttu-id="4c92a-106">Командлет **Get-AzApplicationSecurityGroup** получает группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="4c92a-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="4c92a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c92a-107">EXAMPLES</span></span>

### <span data-ttu-id="4c92a-108">Пример 1: получение всех групп безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="4c92a-108">Example 1: Retrieve all application security groups.</span></span>
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

<span data-ttu-id="4c92a-109">В приведенной выше команде возвращаются все группы безопасности приложений в подписке.</span><span class="sxs-lookup"><span data-stu-id="4c92a-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="4c92a-110">Пример 2: получение групп безопасности приложений в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c92a-110">Example 2: Retrieve application security groups in a resource group.</span></span>
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

<span data-ttu-id="4c92a-111">В приведенной выше команде возвращаются все группы безопасности приложения, которые принадлежат группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4c92a-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="4c92a-112">Пример 3: получение определенной группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="4c92a-112">Example 3: Retrieve a specific application security group.</span></span>
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

<span data-ttu-id="4c92a-113">Приведенная выше команда возвращает группу безопасности приложения MyApplicationSecurityGroup в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4c92a-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="4c92a-114">Пример 4: получение групп безопасности приложений с помощью фильтрации.</span><span class="sxs-lookup"><span data-stu-id="4c92a-114">Example 4: Retrieve application security groups using filtering.</span></span>
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

<span data-ttu-id="4c92a-115">В приведенной выше команде возвращаются все группы безопасности приложения, которые начинаются с "MyApplicationSecurityGroup".</span><span class="sxs-lookup"><span data-stu-id="4c92a-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="4c92a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c92a-116">PARAMETERS</span></span>

### <span data-ttu-id="4c92a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c92a-117">-DefaultProfile</span></span>
<span data-ttu-id="4c92a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c92a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c92a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c92a-119">-Name</span></span>
<span data-ttu-id="4c92a-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c92a-120">The resource name.</span></span>

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

### <span data-ttu-id="4c92a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c92a-121">-ResourceGroupName</span></span>
<span data-ttu-id="4c92a-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c92a-122">The resource group name.</span></span>

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

### <span data-ttu-id="4c92a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c92a-123">CommonParameters</span></span>
<span data-ttu-id="4c92a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c92a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c92a-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c92a-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c92a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c92a-126">INPUTS</span></span>

### <span data-ttu-id="4c92a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4c92a-127">System.String</span></span>

## <span data-ttu-id="4c92a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c92a-128">OUTPUTS</span></span>

### <span data-ttu-id="4c92a-129">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4c92a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="4c92a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c92a-130">NOTES</span></span>

## <span data-ttu-id="4c92a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c92a-131">RELATED LINKS</span></span>

[<span data-ttu-id="4c92a-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4c92a-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="4c92a-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4c92a-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="4c92a-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4c92a-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4c92a-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4c92a-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
