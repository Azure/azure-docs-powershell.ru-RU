---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235131"
---
# <span data-ttu-id="59be0-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59be0-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="59be0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59be0-102">SYNOPSIS</span></span>
<span data-ttu-id="59be0-103">Удаление существующей подписки.</span><span class="sxs-lookup"><span data-stu-id="59be0-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="59be0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59be0-104">SYNTAX</span></span>

### <span data-ttu-id="59be0-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59be0-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59be0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="59be0-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59be0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59be0-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59be0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59be0-108">DESCRIPTION</span></span>
<span data-ttu-id="59be0-109">Командлет **Remove-AzApiManagementSubscription** удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="59be0-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="59be0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59be0-110">EXAMPLES</span></span>

### <span data-ttu-id="59be0-111">Пример 1: Удаление подписки</span><span class="sxs-lookup"><span data-stu-id="59be0-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="59be0-112">Эта команда удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="59be0-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="59be0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59be0-113">PARAMETERS</span></span>

### <span data-ttu-id="59be0-114">-Context</span><span class="sxs-lookup"><span data-stu-id="59be0-114">-Context</span></span>
<span data-ttu-id="59be0-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="59be0-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59be0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59be0-116">-DefaultProfile</span></span>
<span data-ttu-id="59be0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59be0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59be0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59be0-118">-InputObject</span></span>
<span data-ttu-id="59be0-119">Экземпляр PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="59be0-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="59be0-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="59be0-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59be0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59be0-121">-PassThru</span></span>
<span data-ttu-id="59be0-122">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $false, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="59be0-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="59be0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59be0-123">-ResourceId</span></span>
<span data-ttu-id="59be0-124">ИД ResourceId для подписки.</span><span class="sxs-lookup"><span data-stu-id="59be0-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="59be0-125">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="59be0-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59be0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59be0-126">-SubscriptionId</span></span>
<span data-ttu-id="59be0-127">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="59be0-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="59be0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59be0-128">-Confirm</span></span>
<span data-ttu-id="59be0-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59be0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59be0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59be0-130">-WhatIf</span></span>
<span data-ttu-id="59be0-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59be0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59be0-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59be0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59be0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59be0-133">CommonParameters</span></span>
<span data-ttu-id="59be0-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59be0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59be0-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59be0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59be0-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59be0-136">INPUTS</span></span>

### <span data-ttu-id="59be0-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59be0-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59be0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="59be0-138">System.String</span></span>

### <span data-ttu-id="59be0-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59be0-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59be0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59be0-140">OUTPUTS</span></span>

### <span data-ttu-id="59be0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59be0-141">System.Boolean</span></span>

## <span data-ttu-id="59be0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="59be0-142">NOTES</span></span>

## <span data-ttu-id="59be0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59be0-143">RELATED LINKS</span></span>

[<span data-ttu-id="59be0-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59be0-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="59be0-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59be0-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="59be0-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="59be0-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


