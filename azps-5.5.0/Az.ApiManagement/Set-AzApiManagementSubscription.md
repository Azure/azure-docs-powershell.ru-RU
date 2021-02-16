---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244336"
---
# <span data-ttu-id="ce1b3-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ce1b3-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="ce1b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1b3-103">Задает сведения о существующей подписке.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="ce1b3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ce1b3-104">SYNTAX</span></span>

### <span data-ttu-id="ce1b3-105">ByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce1b3-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce1b3-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="ce1b3-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce1b3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce1b3-107">DESCRIPTION</span></span>
<span data-ttu-id="ce1b3-108">На **основе cmdlet Set-AzApiManagementSubscription** задает сведения о существующей подписке.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="ce1b3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ce1b3-109">EXAMPLES</span></span>

### <span data-ttu-id="ce1b3-110">Пример 1. Настройка состояния, первичного и дополнительного ключей для подписки</span><span class="sxs-lookup"><span data-stu-id="ce1b3-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="ce1b3-111">Эта команда задает первичный и дополнительный ключи для подписки и активирует ее.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="ce1b3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce1b3-112">PARAMETERS</span></span>

### <span data-ttu-id="ce1b3-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ce1b3-113">-Context</span></span>
<span data-ttu-id="ce1b3-114">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="ce1b3-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce1b3-115">-DefaultProfile</span></span>
<span data-ttu-id="ce1b3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce1b3-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="ce1b3-117">-ExpiresOn</span></span>
<span data-ttu-id="ce1b3-118">Указывает дату окончания срока действия подписки.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="ce1b3-119">По умолчанию этот параметр имеет значение $Null.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-119">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce1b3-120">-InputObject</span></span>
<span data-ttu-id="ce1b3-121">Экземпляр PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="ce1b3-122">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="ce1b3-122">This parameter is required.</span></span>

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

### <span data-ttu-id="ce1b3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ce1b3-123">-Name</span></span>
<span data-ttu-id="ce1b3-124">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-124">Specifies a subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce1b3-125">-PassThru</span></span>
<span data-ttu-id="ce1b3-126">passthru</span><span class="sxs-lookup"><span data-stu-id="ce1b3-126">passthru</span></span>

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

### <span data-ttu-id="ce1b3-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ce1b3-127">-PrimaryKey</span></span>
<span data-ttu-id="ce1b3-128">Определяет первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="ce1b3-129">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="ce1b3-130">Этот параметр должен иметь длину от 1 до 300 знаков.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-130">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="ce1b3-131">-Scope</span></span>
<span data-ttu-id="ce1b3-132">Область действия подписки, будь то область API /apis/{apiId}, область продуктов /products/{productId} или глобальная область API /apis или глобальная область /.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="ce1b3-133">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="ce1b3-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ce1b3-134">-SecondaryKey</span></span>
<span data-ttu-id="ce1b3-135">Определяет дополнительный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="ce1b3-136">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="ce1b3-137">Этот параметр должен иметь длину от 1 до 300 знаков.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-137">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-138">-State</span><span class="sxs-lookup"><span data-stu-id="ce1b3-138">-State</span></span>
<span data-ttu-id="ce1b3-139">Определяет состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-139">Specifies the subscription state.</span></span>
<span data-ttu-id="ce1b3-140">По умолчанию этот параметр имеет значение $Null.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-140">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="ce1b3-141">-StateComment</span></span>
<span data-ttu-id="ce1b3-142">Указывает комментарий об состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="ce1b3-143">По умолчанию этот параметр имеет значение $Null.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-143">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce1b3-144">-SubscriptionId</span></span>
<span data-ttu-id="ce1b3-145">Определяет ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="ce1b3-146">-UserId</span></span>
<span data-ttu-id="ce1b3-147">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-147">The owner of the subscription.</span></span> <span data-ttu-id="ce1b3-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1b3-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce1b3-149">-Confirm</span></span>
<span data-ttu-id="ce1b3-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce1b3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce1b3-151">-WhatIf</span></span>
<span data-ttu-id="ce1b3-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce1b3-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce1b3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1b3-154">CommonParameters</span></span>
<span data-ttu-id="ce1b3-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce1b3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1b3-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce1b3-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1b3-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce1b3-157">INPUTS</span></span>

### <span data-ttu-id="ce1b3-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ce1b3-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ce1b3-159">System.String</span><span class="sxs-lookup"><span data-stu-id="ce1b3-159">System.String</span></span>

### <span data-ttu-id="ce1b3-160">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="ce1b3-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ce1b3-161">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ce1b3-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ce1b3-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ce1b3-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ce1b3-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ce1b3-163">OUTPUTS</span></span>

### <span data-ttu-id="ce1b3-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ce1b3-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="ce1b3-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ce1b3-165">NOTES</span></span>

## <span data-ttu-id="ce1b3-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce1b3-166">RELATED LINKS</span></span>

[<span data-ttu-id="ce1b3-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ce1b3-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="ce1b3-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ce1b3-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="ce1b3-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ce1b3-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


