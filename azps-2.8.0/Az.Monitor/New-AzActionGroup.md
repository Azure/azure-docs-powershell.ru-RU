---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 47ab8423de29a1cdfeb7edb268560bb28cfc8ac7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411404"
---
# <span data-ttu-id="e91e0-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e91e0-101">New-AzActionGroup</span></span>

## <span data-ttu-id="e91e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e91e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e91e0-103">Создает объект ссылки ActionGroup в памяти.</span><span class="sxs-lookup"><span data-stu-id="e91e0-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="e91e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e91e0-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e91e0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e91e0-105">DESCRIPTION</span></span>
<span data-ttu-id="e91e0-106">Для **этого в памяти создается** объект ссылки на группу действий.</span><span class="sxs-lookup"><span data-stu-id="e91e0-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="e91e0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e91e0-107">EXAMPLES</span></span>

### <span data-ttu-id="e91e0-108">Пример 1. Создание справочного объекта группы действий в памяти</span><span class="sxs-lookup"><span data-stu-id="e91e0-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="e91e0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e91e0-109">PARAMETERS</span></span>

### <span data-ttu-id="e91e0-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="e91e0-110">-ActionGroupId</span></span>
<span data-ttu-id="e91e0-111">ИД или имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="e91e0-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="e91e0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91e0-112">-DefaultProfile</span></span>
<span data-ttu-id="e91e0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e91e0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e91e0-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="e91e0-114">-WebhookProperty</span></span>
<span data-ttu-id="e91e0-115">Свойства веб-приложения группы действий</span><span class="sxs-lookup"><span data-stu-id="e91e0-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="e91e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91e0-116">CommonParameters</span></span>
<span data-ttu-id="e91e0-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91e0-118">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e91e0-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91e0-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e91e0-119">INPUTS</span></span>

### <span data-ttu-id="e91e0-120">System.String</span><span class="sxs-lookup"><span data-stu-id="e91e0-120">System.String</span></span>

### <span data-ttu-id="e91e0-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e91e0-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e91e0-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e91e0-122">OUTPUTS</span></span>

### <span data-ttu-id="e91e0-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="e91e0-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="e91e0-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e91e0-124">NOTES</span></span>

## <span data-ttu-id="e91e0-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e91e0-125">RELATED LINKS</span></span>

[<span data-ttu-id="e91e0-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e91e0-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e91e0-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e91e0-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="e91e0-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e91e0-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="e91e0-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e91e0-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="e91e0-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e91e0-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)



