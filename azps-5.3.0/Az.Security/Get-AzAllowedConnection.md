---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517790"
---
# <span data-ttu-id="24007-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="24007-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="24007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24007-102">SYNOPSIS</span></span>
<span data-ttu-id="24007-103">Используется для отображения разрешенного трафика между ресурсами подписки</span><span class="sxs-lookup"><span data-stu-id="24007-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="24007-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24007-104">SYNTAX</span></span>

### <span data-ttu-id="24007-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24007-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24007-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="24007-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24007-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24007-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24007-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24007-108">DESCRIPTION</span></span>
<span data-ttu-id="24007-109">Возвращает список всех возможных трафика между ресурсами для подписки и расположения в зависимости от типа подключения.</span><span class="sxs-lookup"><span data-stu-id="24007-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="24007-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24007-110">EXAMPLES</span></span>

### <span data-ttu-id="24007-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="24007-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="24007-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="24007-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="24007-113">Возвращает список всех возможных трафика между ресурсами для подписки и расположения в зависимости от типа подключения.</span><span class="sxs-lookup"><span data-stu-id="24007-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="24007-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24007-114">PARAMETERS</span></span>

### <span data-ttu-id="24007-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24007-115">-DefaultProfile</span></span>
<span data-ttu-id="24007-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24007-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24007-117">-Location</span><span class="sxs-lookup"><span data-stu-id="24007-117">-Location</span></span>
<span data-ttu-id="24007-118">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="24007-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24007-119">-Name</span><span class="sxs-lookup"><span data-stu-id="24007-119">-Name</span></span>
<span data-ttu-id="24007-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="24007-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24007-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24007-121">-ResourceGroupName</span></span>
<span data-ttu-id="24007-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24007-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24007-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24007-123">-ResourceId</span></span>
<span data-ttu-id="24007-124">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="24007-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24007-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24007-125">CommonParameters</span></span>
<span data-ttu-id="24007-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24007-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24007-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24007-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24007-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24007-128">INPUTS</span></span>

### <span data-ttu-id="24007-129">System.String</span><span class="sxs-lookup"><span data-stu-id="24007-129">System.String</span></span>

## <span data-ttu-id="24007-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24007-130">OUTPUTS</span></span>

### <span data-ttu-id="24007-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="24007-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="24007-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24007-132">NOTES</span></span>

## <span data-ttu-id="24007-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24007-133">RELATED LINKS</span></span>
