---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 99fb63a5dd4ba60b44e96139418a76701334444e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250036"
---
# <span data-ttu-id="4fe08-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="4fe08-101">New-AzActionGroup</span></span>

## <span data-ttu-id="4fe08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fe08-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe08-103">Создает объект ссылки на ActionGroup в памяти.</span><span class="sxs-lookup"><span data-stu-id="4fe08-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="4fe08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fe08-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fe08-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fe08-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe08-106">Командлет **New-AzActionGroup** создает объект ссылки на группу действий в памяти.</span><span class="sxs-lookup"><span data-stu-id="4fe08-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="4fe08-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fe08-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe08-108">Пример 1: создание объекта ссылки на группу действий в памяти</span><span class="sxs-lookup"><span data-stu-id="4fe08-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="4fe08-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fe08-109">PARAMETERS</span></span>

### <span data-ttu-id="4fe08-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="4fe08-110">-ActionGroupId</span></span>
<span data-ttu-id="4fe08-111">Идентификатор или имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="4fe08-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="4fe08-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe08-112">-DefaultProfile</span></span>
<span data-ttu-id="4fe08-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4fe08-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fe08-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="4fe08-114">-WebhookProperty</span></span>
<span data-ttu-id="4fe08-115">Свойства веб-перехватчика группы "действия"</span><span class="sxs-lookup"><span data-stu-id="4fe08-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="4fe08-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe08-116">CommonParameters</span></span>
<span data-ttu-id="4fe08-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fe08-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe08-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fe08-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe08-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fe08-119">INPUTS</span></span>

### <span data-ttu-id="4fe08-120">System. String</span><span class="sxs-lookup"><span data-stu-id="4fe08-120">System.String</span></span>

### <span data-ttu-id="4fe08-121">System. Collections. Generic. Dictionary "2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]; [System. String; System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4fe08-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4fe08-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fe08-122">OUTPUTS</span></span>

### <span data-ttu-id="4fe08-123">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="4fe08-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="4fe08-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fe08-124">NOTES</span></span>

## <span data-ttu-id="4fe08-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fe08-125">RELATED LINKS</span></span>

[<span data-ttu-id="4fe08-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4fe08-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="4fe08-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4fe08-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="4fe08-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4fe08-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="4fe08-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4fe08-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="4fe08-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4fe08-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="4fe08-131">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4fe08-131">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
