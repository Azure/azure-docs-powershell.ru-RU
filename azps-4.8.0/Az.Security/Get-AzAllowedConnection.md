---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078761"
---
# <span data-ttu-id="787e5-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="787e5-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="787e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="787e5-102">SYNOPSIS</span></span>
<span data-ttu-id="787e5-103">Используется для отображения разрешенного трафика между ресурсами для подписки</span><span class="sxs-lookup"><span data-stu-id="787e5-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="787e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="787e5-104">SYNTAX</span></span>

### <span data-ttu-id="787e5-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="787e5-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="787e5-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="787e5-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="787e5-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="787e5-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="787e5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="787e5-108">DESCRIPTION</span></span>
<span data-ttu-id="787e5-109">Получает список всех возможных трафиков между ресурсами для подписки и местоположения на основе типа соединения.</span><span class="sxs-lookup"><span data-stu-id="787e5-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="787e5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="787e5-110">EXAMPLES</span></span>

### <span data-ttu-id="787e5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="787e5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="787e5-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="787e5-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="787e5-113">Получает список всех возможных трафиков между ресурсами для подписки и местоположения на основе типа соединения.</span><span class="sxs-lookup"><span data-stu-id="787e5-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="787e5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="787e5-114">PARAMETERS</span></span>

### <span data-ttu-id="787e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787e5-115">-DefaultProfile</span></span>
<span data-ttu-id="787e5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="787e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="787e5-117">-Location</span><span class="sxs-lookup"><span data-stu-id="787e5-117">-Location</span></span>
<span data-ttu-id="787e5-118">Поиска.</span><span class="sxs-lookup"><span data-stu-id="787e5-118">Location.</span></span>

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

### <span data-ttu-id="787e5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="787e5-119">-Name</span></span>
<span data-ttu-id="787e5-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="787e5-120">Resource name.</span></span>

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

### <span data-ttu-id="787e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="787e5-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="787e5-122">Resource group name.</span></span>

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

### <span data-ttu-id="787e5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="787e5-123">-ResourceId</span></span>
<span data-ttu-id="787e5-124">Идентификатор ресурса безопасности, для которого нужно вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="787e5-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="787e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787e5-125">CommonParameters</span></span>
<span data-ttu-id="787e5-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="787e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787e5-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="787e5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787e5-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="787e5-128">INPUTS</span></span>

### <span data-ttu-id="787e5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="787e5-129">System.String</span></span>

## <span data-ttu-id="787e5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="787e5-130">OUTPUTS</span></span>

### <span data-ttu-id="787e5-131">Microsoft. Azure. Commands. Security. Models. AllowedConnection. PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="787e5-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="787e5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="787e5-132">NOTES</span></span>

## <span data-ttu-id="787e5-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="787e5-133">RELATED LINKS</span></span>