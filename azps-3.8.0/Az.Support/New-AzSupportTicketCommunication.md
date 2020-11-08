---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066130"
---
# <span data-ttu-id="95f14-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="95f14-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="95f14-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95f14-102">SYNOPSIS</span></span>
<span data-ttu-id="95f14-103">Создание нового общения с билетами поддержки.</span><span class="sxs-lookup"><span data-stu-id="95f14-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="95f14-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95f14-104">SYNTAX</span></span>

### <span data-ttu-id="95f14-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95f14-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95f14-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95f14-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95f14-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f14-107">DESCRIPTION</span></span>
<span data-ttu-id="95f14-108">Добавляет новый клиентский связь с билетом службы поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="95f14-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="95f14-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95f14-109">EXAMPLES</span></span>

### <span data-ttu-id="95f14-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95f14-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="95f14-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95f14-111">PARAMETERS</span></span>

### <span data-ttu-id="95f14-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95f14-112">-AsJob</span></span>
<span data-ttu-id="95f14-113">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="95f14-113">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-114">-Body</span><span class="sxs-lookup"><span data-stu-id="95f14-114">-Body</span></span>
<span data-ttu-id="95f14-115">Текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="95f14-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f14-116">-DefaultProfile</span></span>
<span data-ttu-id="95f14-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95f14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95f14-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95f14-118">-Name</span></span>
<span data-ttu-id="95f14-119">Имя коммуникационного ресурса.</span><span class="sxs-lookup"><span data-stu-id="95f14-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-120">-Отправитель</span><span class="sxs-lookup"><span data-stu-id="95f14-120">-Sender</span></span>
<span data-ttu-id="95f14-121">Адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="95f14-121">Email address of the sender.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-122">-Тема</span><span class="sxs-lookup"><span data-stu-id="95f14-122">-Subject</span></span>
<span data-ttu-id="95f14-123">Тема общения.</span><span class="sxs-lookup"><span data-stu-id="95f14-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="95f14-124">-SupportTicketName</span></span>
<span data-ttu-id="95f14-125">Имя билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="95f14-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="95f14-126">-SupportTicketObject</span></span>
<span data-ttu-id="95f14-127">Объект билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="95f14-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95f14-128">-Confirm</span></span>
<span data-ttu-id="95f14-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95f14-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95f14-130">-WhatIf</span></span>
<span data-ttu-id="95f14-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95f14-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95f14-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95f14-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f14-133">CommonParameters</span></span>
<span data-ttu-id="95f14-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95f14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f14-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95f14-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f14-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95f14-136">INPUTS</span></span>

### <span data-ttu-id="95f14-137">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="95f14-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="95f14-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f14-138">OUTPUTS</span></span>

### <span data-ttu-id="95f14-139">Microsoft. Azure. Commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="95f14-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="95f14-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="95f14-140">NOTES</span></span>

## <span data-ttu-id="95f14-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95f14-141">RELATED LINKS</span></span>
