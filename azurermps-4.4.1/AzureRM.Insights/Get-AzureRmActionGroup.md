---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 4edb403452d262705fe8fa61691ac77ba4524977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569404"
---
# <span data-ttu-id="6a06c-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6a06c-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="6a06c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a06c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a06c-103">Получает группу действий.</span><span class="sxs-lookup"><span data-stu-id="6a06c-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a06c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a06c-104">SYNTAX</span></span>

### <span data-ttu-id="6a06c-105">BySubscriptionOrResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a06c-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a06c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6a06c-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a06c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a06c-107">DESCRIPTION</span></span>
<span data-ttu-id="6a06c-108">Командлет **Get-AzureRmActionGroup** получает одну или несколько групп действий.</span><span class="sxs-lookup"><span data-stu-id="6a06c-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="6a06c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a06c-109">EXAMPLES</span></span>

### <span data-ttu-id="6a06c-110">Пример 1: получение группы действий по коду подписки</span><span class="sxs-lookup"><span data-stu-id="6a06c-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="6a06c-111">Эта команда выводит список всех групп действий для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="6a06c-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="6a06c-112">Пример 2: получение групп действий для указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6a06c-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="6a06c-113">Эта команда перечисляет группы действий для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a06c-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="6a06c-114">Пример 3: получение группы действий.</span><span class="sxs-lookup"><span data-stu-id="6a06c-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="6a06c-115">Эта команда перечисляет один (список с одной группой действий).</span><span class="sxs-lookup"><span data-stu-id="6a06c-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="6a06c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a06c-116">PARAMETERS</span></span>

### <span data-ttu-id="6a06c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6a06c-117">-Name</span></span>
<span data-ttu-id="6a06c-118">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="6a06c-118">The name of the action group.</span></span>

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

### <span data-ttu-id="6a06c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a06c-119">-DefaultProfile</span></span>
<span data-ttu-id="6a06c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a06c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a06c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a06c-121">-ResourceGroupName</span></span>
<span data-ttu-id="6a06c-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6a06c-122">The resource group name</span></span>

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

### <span data-ttu-id="6a06c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a06c-123">CommonParameters</span></span>
<span data-ttu-id="6a06c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a06c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a06c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a06c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a06c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a06c-126">INPUTS</span></span>

### <span data-ttu-id="6a06c-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="6a06c-127">None</span></span>

## <span data-ttu-id="6a06c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a06c-128">OUTPUTS</span></span>

### <span data-ttu-id="6a06c-129"><System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource]</span><span class="sxs-lookup"><span data-stu-id="6a06c-129"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource]</span></span>

### <span data-ttu-id="6a06c-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="6a06c-130">None</span></span>

## <span data-ttu-id="6a06c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a06c-131">NOTES</span></span>

## <span data-ttu-id="6a06c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a06c-132">RELATED LINKS</span></span>

<span data-ttu-id="6a06c-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="6a06c-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
