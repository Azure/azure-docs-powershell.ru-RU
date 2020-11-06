---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569407"
---
# <span data-ttu-id="ba403-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba403-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="ba403-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba403-102">SYNOPSIS</span></span>
<span data-ttu-id="ba403-103">Получает один или несколько ресурсов для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="ba403-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba403-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba403-104">SYNTAX</span></span>

### <span data-ttu-id="ba403-105">Параметры по умолчанию для уведомления о получении журнала активности</span><span class="sxs-lookup"><span data-stu-id="ba403-105">Default parameters for get an activity log alert</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba403-106">Параметры, позволяющие убедиться, что группа ресурсов задана при присвоении имени</span><span class="sxs-lookup"><span data-stu-id="ba403-106">Parameters to make sure the resource group is given when the name is given</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba403-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba403-107">DESCRIPTION</span></span>
<span data-ttu-id="ba403-108">Командлет **Get-AzureRmActivityLogAlert** получает один или несколько ресурсов для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="ba403-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="ba403-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba403-109">EXAMPLES</span></span>

### <span data-ttu-id="ba403-110">Пример 1: получение уведомлений журнала активности по ИДЕНТИФИКАТОРу подписки</span><span class="sxs-lookup"><span data-stu-id="ba403-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="ba403-111">Эта команда выводит список всех оповещений журнала активности для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ba403-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="ba403-112">Пример 2: получение оповещений журнала активности для указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ba403-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="ba403-113">Эта команда перечисляет оповещения журнала активности для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba403-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="ba403-114">Пример 3: Получение оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="ba403-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="ba403-115">Эта команда перечисляет один (список, в котором есть один элемент) оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="ba403-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="ba403-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba403-116">PARAMETERS</span></span>

### <span data-ttu-id="ba403-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba403-117">-Name</span></span>
<span data-ttu-id="ba403-118">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="ba403-118">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba403-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba403-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba403-120">Имя группы ресурсов, в которой находится ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="ba403-120">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="ba403-121">Если имя не равно null или пустое, этот параметр должен содержать и не пустую строку.</span><span class="sxs-lookup"><span data-stu-id="ba403-121">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba403-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba403-122">-DefaultProfile</span></span>
<span data-ttu-id="ba403-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba403-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba403-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba403-124">CommonParameters</span></span>
<span data-ttu-id="ba403-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba403-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba403-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba403-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba403-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba403-127">INPUTS</span></span>

### <span data-ttu-id="ba403-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="ba403-128">None</span></span>

## <span data-ttu-id="ba403-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba403-129">OUTPUTS</span></span>

### <span data-ttu-id="ba403-130"><System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="ba403-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="ba403-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="ba403-131">None</span></span>

## <span data-ttu-id="ba403-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba403-132">NOTES</span></span>

## <span data-ttu-id="ba403-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba403-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba403-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba403-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ba403-135">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba403-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ba403-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba403-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ba403-137">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="ba403-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="ba403-138">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="ba403-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
