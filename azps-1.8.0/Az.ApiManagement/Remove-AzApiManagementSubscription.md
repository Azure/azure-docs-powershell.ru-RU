---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901629"
---
# <span data-ttu-id="1f0a2-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f0a2-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="1f0a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0a2-103">Удаление существующей подписки.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="1f0a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f0a2-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f0a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f0a2-105">DESCRIPTION</span></span>
<span data-ttu-id="1f0a2-106">Командлет **Remove-AzApiManagementSubscription** удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="1f0a2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f0a2-107">EXAMPLES</span></span>

### <span data-ttu-id="1f0a2-108">Пример 1: Удаление подписки</span><span class="sxs-lookup"><span data-stu-id="1f0a2-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="1f0a2-109">Эта команда удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="1f0a2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f0a2-110">PARAMETERS</span></span>

### <span data-ttu-id="1f0a2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1f0a2-111">-Context</span></span>
<span data-ttu-id="1f0a2-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1f0a2-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f0a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0a2-113">-DefaultProfile</span></span>
<span data-ttu-id="1f0a2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f0a2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f0a2-115">-PassThru</span></span>
<span data-ttu-id="1f0a2-116">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $false, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f0a2-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f0a2-117">-SubscriptionId</span></span>
<span data-ttu-id="1f0a2-118">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="1f0a2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f0a2-119">-Confirm</span></span>
<span data-ttu-id="1f0a2-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f0a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f0a2-121">-WhatIf</span></span>
<span data-ttu-id="1f0a2-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f0a2-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f0a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0a2-124">CommonParameters</span></span>
<span data-ttu-id="1f0a2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f0a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0a2-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f0a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0a2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f0a2-127">INPUTS</span></span>

### <span data-ttu-id="1f0a2-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1f0a2-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1f0a2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1f0a2-129">System.String</span></span>

### <span data-ttu-id="1f0a2-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f0a2-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1f0a2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f0a2-131">OUTPUTS</span></span>

### <span data-ttu-id="1f0a2-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f0a2-132">System.Boolean</span></span>

## <span data-ttu-id="1f0a2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f0a2-133">NOTES</span></span>

## <span data-ttu-id="1f0a2-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f0a2-134">RELATED LINKS</span></span>

[<span data-ttu-id="1f0a2-135">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f0a2-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="1f0a2-136">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f0a2-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="1f0a2-137">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="1f0a2-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


