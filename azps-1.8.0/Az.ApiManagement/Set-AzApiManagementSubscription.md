---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731666"
---
# <span data-ttu-id="39939-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="39939-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="39939-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39939-102">SYNOPSIS</span></span>
<span data-ttu-id="39939-103">Задает сведения о существующем подписке.</span><span class="sxs-lookup"><span data-stu-id="39939-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="39939-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39939-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39939-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39939-105">DESCRIPTION</span></span>
<span data-ttu-id="39939-106">Командлет **Set-AzApiManagementSubscription** задает существующие сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="39939-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="39939-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39939-107">EXAMPLES</span></span>

### <span data-ttu-id="39939-108">Пример 1: Настройка состояния и первичных и вторичных ключей для подписки</span><span class="sxs-lookup"><span data-stu-id="39939-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="39939-109">Эта команда задает первичные и вторичные ключи для подписки и активирует ее.</span><span class="sxs-lookup"><span data-stu-id="39939-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="39939-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39939-110">PARAMETERS</span></span>

### <span data-ttu-id="39939-111">-Context</span><span class="sxs-lookup"><span data-stu-id="39939-111">-Context</span></span>
<span data-ttu-id="39939-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="39939-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="39939-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39939-113">-DefaultProfile</span></span>
<span data-ttu-id="39939-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39939-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39939-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="39939-115">-ExpiresOn</span></span>
<span data-ttu-id="39939-116">Указывает дату окончания срока действия подписки.</span><span class="sxs-lookup"><span data-stu-id="39939-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="39939-117">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="39939-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="39939-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39939-118">-Name</span></span>
<span data-ttu-id="39939-119">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="39939-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="39939-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39939-120">-PassThru</span></span>
<span data-ttu-id="39939-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="39939-121">passthru</span></span>

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

### <span data-ttu-id="39939-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="39939-122">-PrimaryKey</span></span>
<span data-ttu-id="39939-123">Указывает первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="39939-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="39939-124">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="39939-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="39939-125">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="39939-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="39939-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="39939-126">-SecondaryKey</span></span>
<span data-ttu-id="39939-127">Задает вторичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="39939-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="39939-128">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="39939-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="39939-129">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="39939-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="39939-130">-State</span><span class="sxs-lookup"><span data-stu-id="39939-130">-State</span></span>
<span data-ttu-id="39939-131">Указывает состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="39939-131">Specifies the subscription state.</span></span>
<span data-ttu-id="39939-132">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="39939-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="39939-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="39939-133">-StateComment</span></span>
<span data-ttu-id="39939-134">Указывает Примечание о состоянии подписки.</span><span class="sxs-lookup"><span data-stu-id="39939-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="39939-135">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="39939-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="39939-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39939-136">-SubscriptionId</span></span>
<span data-ttu-id="39939-137">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="39939-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="39939-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39939-138">CommonParameters</span></span>
<span data-ttu-id="39939-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39939-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39939-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39939-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39939-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39939-141">INPUTS</span></span>

### <span data-ttu-id="39939-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="39939-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="39939-143">System. String</span><span class="sxs-lookup"><span data-stu-id="39939-143">System.String</span></span>

### <span data-ttu-id="39939-144">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="39939-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="39939-145">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="39939-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="39939-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="39939-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39939-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39939-147">OUTPUTS</span></span>

### <span data-ttu-id="39939-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="39939-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="39939-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="39939-149">NOTES</span></span>

## <span data-ttu-id="39939-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39939-150">RELATED LINKS</span></span>

[<span data-ttu-id="39939-151">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="39939-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="39939-152">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="39939-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="39939-153">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="39939-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


