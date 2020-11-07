---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7a881b6479561ac7a616158c8054bff592209289
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915313"
---
# <span data-ttu-id="a5846-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a5846-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="a5846-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5846-102">SYNOPSIS</span></span>
<span data-ttu-id="a5846-103">Получает группу действий.</span><span class="sxs-lookup"><span data-stu-id="a5846-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5846-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5846-104">SYNTAX</span></span>

### <span data-ttu-id="a5846-105">BySubscriptionOrResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5846-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5846-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a5846-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5846-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5846-107">DESCRIPTION</span></span>
<span data-ttu-id="a5846-108">Командлет **Get-AzureRmActionGroup** получает одну или несколько групп действий.</span><span class="sxs-lookup"><span data-stu-id="a5846-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="a5846-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5846-109">EXAMPLES</span></span>

### <span data-ttu-id="a5846-110">Пример 1: получение группы действий по коду подписки</span><span class="sxs-lookup"><span data-stu-id="a5846-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="a5846-111">Эта команда выводит список всех групп действий для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="a5846-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="a5846-112">Пример 2: получение групп действий для указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a5846-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="a5846-113">Эта команда перечисляет группы действий для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5846-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="a5846-114">Пример 3: получение группы действий.</span><span class="sxs-lookup"><span data-stu-id="a5846-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="a5846-115">Эта команда перечисляет один (список с одной группой действий).</span><span class="sxs-lookup"><span data-stu-id="a5846-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="a5846-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5846-116">PARAMETERS</span></span>

### <span data-ttu-id="a5846-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5846-117">-DefaultProfile</span></span>
<span data-ttu-id="a5846-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a5846-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5846-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5846-119">-Name</span></span>
<span data-ttu-id="a5846-120">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="a5846-120">The name of the action group.</span></span>

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

### <span data-ttu-id="a5846-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5846-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5846-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a5846-122">The resource group name</span></span>

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

### <span data-ttu-id="a5846-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5846-123">CommonParameters</span></span>
<span data-ttu-id="a5846-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5846-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5846-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5846-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5846-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5846-126">INPUTS</span></span>

### <span data-ttu-id="a5846-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a5846-127">System.String</span></span>

## <span data-ttu-id="a5846-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5846-128">OUTPUTS</span></span>

### <span data-ttu-id="a5846-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="a5846-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="a5846-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5846-130">NOTES</span></span>

## <span data-ttu-id="a5846-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5846-131">RELATED LINKS</span></span>

<span data-ttu-id="a5846-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="a5846-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
