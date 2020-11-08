---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242658"
---
# <span data-ttu-id="05e51-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="05e51-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="05e51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05e51-102">SYNOPSIS</span></span>
<span data-ttu-id="05e51-103">Задает сведения о существующем подписке.</span><span class="sxs-lookup"><span data-stu-id="05e51-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="05e51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05e51-104">SYNTAX</span></span>

### <span data-ttu-id="05e51-105">ByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05e51-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05e51-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="05e51-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05e51-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05e51-107">DESCRIPTION</span></span>
<span data-ttu-id="05e51-108">Командлет **Set-AzApiManagementSubscription** задает существующие сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="05e51-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="05e51-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05e51-109">EXAMPLES</span></span>

### <span data-ttu-id="05e51-110">Пример 1: Настройка состояния и первичных и вторичных ключей для подписки</span><span class="sxs-lookup"><span data-stu-id="05e51-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="05e51-111">Эта команда задает первичные и вторичные ключи для подписки и активирует ее.</span><span class="sxs-lookup"><span data-stu-id="05e51-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="05e51-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05e51-112">PARAMETERS</span></span>

### <span data-ttu-id="05e51-113">-Context</span><span class="sxs-lookup"><span data-stu-id="05e51-113">-Context</span></span>
<span data-ttu-id="05e51-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="05e51-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="05e51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e51-115">-DefaultProfile</span></span>
<span data-ttu-id="05e51-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05e51-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05e51-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="05e51-117">-ExpiresOn</span></span>
<span data-ttu-id="05e51-118">Указывает дату окончания срока действия подписки.</span><span class="sxs-lookup"><span data-stu-id="05e51-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="05e51-119">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="05e51-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="05e51-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05e51-120">-InputObject</span></span>
<span data-ttu-id="05e51-121">Экземпляр PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="05e51-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="05e51-122">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="05e51-122">This parameter is required.</span></span>

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

### <span data-ttu-id="05e51-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05e51-123">-Name</span></span>
<span data-ttu-id="05e51-124">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="05e51-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="05e51-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05e51-125">-PassThru</span></span>
<span data-ttu-id="05e51-126">PassThru</span><span class="sxs-lookup"><span data-stu-id="05e51-126">passthru</span></span>

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

### <span data-ttu-id="05e51-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="05e51-127">-PrimaryKey</span></span>
<span data-ttu-id="05e51-128">Указывает первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="05e51-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="05e51-129">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="05e51-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="05e51-130">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="05e51-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="05e51-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="05e51-131">-Scope</span></span>
<span data-ttu-id="05e51-132">Область действия подписки, независимо от того, является ли она областью API/apis/{apiId} или областью продукта/products/{productId} или Global API Scope/APIs или Global Scope/.</span><span class="sxs-lookup"><span data-stu-id="05e51-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="05e51-133">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="05e51-133">This parameter is required.</span></span>

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

### <span data-ttu-id="05e51-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="05e51-134">-SecondaryKey</span></span>
<span data-ttu-id="05e51-135">Задает вторичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="05e51-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="05e51-136">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="05e51-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="05e51-137">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="05e51-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="05e51-138">-State</span><span class="sxs-lookup"><span data-stu-id="05e51-138">-State</span></span>
<span data-ttu-id="05e51-139">Указывает состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="05e51-139">Specifies the subscription state.</span></span>
<span data-ttu-id="05e51-140">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="05e51-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="05e51-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="05e51-141">-StateComment</span></span>
<span data-ttu-id="05e51-142">Указывает Примечание о состоянии подписки.</span><span class="sxs-lookup"><span data-stu-id="05e51-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="05e51-143">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="05e51-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="05e51-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05e51-144">-SubscriptionId</span></span>
<span data-ttu-id="05e51-145">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="05e51-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="05e51-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="05e51-146">-UserId</span></span>
<span data-ttu-id="05e51-147">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="05e51-147">The owner of the subscription.</span></span> <span data-ttu-id="05e51-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="05e51-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="05e51-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05e51-149">-Confirm</span></span>
<span data-ttu-id="05e51-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05e51-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05e51-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05e51-151">-WhatIf</span></span>
<span data-ttu-id="05e51-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05e51-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05e51-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05e51-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05e51-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e51-154">CommonParameters</span></span>
<span data-ttu-id="05e51-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05e51-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e51-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05e51-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e51-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05e51-157">INPUTS</span></span>

### <span data-ttu-id="05e51-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="05e51-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05e51-159">System. String</span><span class="sxs-lookup"><span data-stu-id="05e51-159">System.String</span></span>

### <span data-ttu-id="05e51-160">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="05e51-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="05e51-161">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="05e51-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="05e51-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05e51-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05e51-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05e51-163">OUTPUTS</span></span>

### <span data-ttu-id="05e51-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="05e51-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="05e51-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="05e51-165">NOTES</span></span>

## <span data-ttu-id="05e51-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05e51-166">RELATED LINKS</span></span>

[<span data-ttu-id="05e51-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="05e51-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="05e51-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="05e51-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="05e51-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="05e51-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

