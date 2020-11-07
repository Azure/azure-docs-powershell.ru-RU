---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: b2f9738518f446b9cf5bfbefe0c7025bb3351628
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913372"
---
# <span data-ttu-id="7769e-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7769e-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="7769e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7769e-102">SYNOPSIS</span></span>
<span data-ttu-id="7769e-103">Создает объект ссылки на ActionGroup в памяти.</span><span class="sxs-lookup"><span data-stu-id="7769e-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7769e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7769e-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7769e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7769e-105">DESCRIPTION</span></span>
<span data-ttu-id="7769e-106">Командлет **New-AzureRmActionGroup** создает объект ссылки на группу действий в памяти.</span><span class="sxs-lookup"><span data-stu-id="7769e-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="7769e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7769e-107">EXAMPLES</span></span>

### <span data-ttu-id="7769e-108">Пример 1: создание объекта ссылки на группу действий в памяти</span><span class="sxs-lookup"><span data-stu-id="7769e-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="7769e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7769e-109">PARAMETERS</span></span>

### <span data-ttu-id="7769e-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="7769e-110">-ActionGroupId</span></span>
<span data-ttu-id="7769e-111">Идентификатор или имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="7769e-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7769e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7769e-112">-DefaultProfile</span></span>
<span data-ttu-id="7769e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7769e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7769e-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="7769e-114">-WebhookProperty</span></span>
<span data-ttu-id="7769e-115">Свойства веб-перехватчика группы "действия"</span><span class="sxs-lookup"><span data-stu-id="7769e-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7769e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7769e-116">CommonParameters</span></span>
<span data-ttu-id="7769e-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7769e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7769e-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7769e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7769e-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7769e-119">INPUTS</span></span>

### <span data-ttu-id="7769e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7769e-120">System.String</span></span>

### <span data-ttu-id="7769e-121">System. Collections. Generic. Dictionary "2 [[System. String, mscorlib, Version = 4.0.0.0, культура = нейтраль, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, культура = нейтральная, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7769e-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7769e-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7769e-122">OUTPUTS</span></span>

### <span data-ttu-id="7769e-123">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="7769e-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="7769e-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="7769e-124">NOTES</span></span>

## <span data-ttu-id="7769e-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7769e-125">RELATED LINKS</span></span>

[<span data-ttu-id="7769e-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7769e-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7769e-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7769e-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7769e-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7769e-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7769e-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7769e-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7769e-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7769e-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="7769e-131">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="7769e-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

