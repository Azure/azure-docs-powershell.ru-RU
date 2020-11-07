---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: ca4229f5f882b1065c6f39b8c162bb91b90b835d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910258"
---
# <span data-ttu-id="9d833-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="9d833-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="9d833-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d833-102">SYNOPSIS</span></span>
<span data-ttu-id="9d833-103">Получает группу действий.</span><span class="sxs-lookup"><span data-stu-id="9d833-103">Gets action group(s).</span></span>

## <span data-ttu-id="9d833-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d833-104">SYNTAX</span></span>

### <span data-ttu-id="9d833-105">BySubscriptionOrResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d833-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d833-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9d833-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d833-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d833-107">DESCRIPTION</span></span>
<span data-ttu-id="9d833-108">Командлет **Get-AzActionGroup** получает одну или несколько групп действий.</span><span class="sxs-lookup"><span data-stu-id="9d833-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="9d833-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d833-109">EXAMPLES</span></span>

### <span data-ttu-id="9d833-110">Пример 1: получение группы действий по коду подписки</span><span class="sxs-lookup"><span data-stu-id="9d833-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="9d833-111">Эта команда выводит список всех групп действий для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="9d833-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="9d833-112">Пример 2: получение групп действий для указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9d833-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="9d833-113">Эта команда перечисляет группы действий для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d833-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="9d833-114">Пример 3: получение группы действий.</span><span class="sxs-lookup"><span data-stu-id="9d833-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="9d833-115">Эта команда перечисляет один (список с одной группой действий).</span><span class="sxs-lookup"><span data-stu-id="9d833-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="9d833-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d833-116">PARAMETERS</span></span>

### <span data-ttu-id="9d833-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d833-117">-DefaultProfile</span></span>
<span data-ttu-id="9d833-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9d833-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d833-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d833-119">-Name</span></span>
<span data-ttu-id="9d833-120">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="9d833-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d833-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d833-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d833-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9d833-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d833-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d833-123">CommonParameters</span></span>
<span data-ttu-id="9d833-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d833-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d833-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d833-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d833-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d833-126">INPUTS</span></span>

### <span data-ttu-id="9d833-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9d833-127">System.String</span></span>

## <span data-ttu-id="9d833-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d833-128">OUTPUTS</span></span>

### <span data-ttu-id="9d833-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="9d833-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="9d833-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d833-130">NOTES</span></span>

## <span data-ttu-id="9d833-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d833-131">RELATED LINKS</span></span>

<span data-ttu-id="9d833-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="9d833-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
