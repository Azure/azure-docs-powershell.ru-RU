---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: c747d85f87e88c3f72ae86c8bcef771b3e42c91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558604"
---
# <span data-ttu-id="9d54a-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d54a-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="9d54a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d54a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d54a-103">Задает сведения о существующем подписке.</span><span class="sxs-lookup"><span data-stu-id="9d54a-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d54a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d54a-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d54a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d54a-105">DESCRIPTION</span></span>
<span data-ttu-id="9d54a-106">Командлет **Set-AzureRmApiManagementSubscription** задает существующие сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="9d54a-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="9d54a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d54a-107">EXAMPLES</span></span>

### <span data-ttu-id="9d54a-108">Пример 1: Настройка состояния и первичных и вторичных ключей для подписки</span><span class="sxs-lookup"><span data-stu-id="9d54a-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="9d54a-109">Эта команда задает первичные и вторичные ключи для подписки и активирует ее.</span><span class="sxs-lookup"><span data-stu-id="9d54a-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="9d54a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d54a-110">PARAMETERS</span></span>

### <span data-ttu-id="9d54a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9d54a-111">-Context</span></span>
<span data-ttu-id="9d54a-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9d54a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9d54a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d54a-113">-DefaultProfile</span></span>
<span data-ttu-id="9d54a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d54a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d54a-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="9d54a-115">-ExpiresOn</span></span>
<span data-ttu-id="9d54a-116">Указывает дату окончания срока действия подписки.</span><span class="sxs-lookup"><span data-stu-id="9d54a-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="9d54a-117">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9d54a-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="9d54a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d54a-118">-Name</span></span>
<span data-ttu-id="9d54a-119">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="9d54a-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="9d54a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d54a-120">-PassThru</span></span>
<span data-ttu-id="9d54a-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="9d54a-121">passthru</span></span>

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

### <span data-ttu-id="9d54a-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9d54a-122">-PrimaryKey</span></span>
<span data-ttu-id="9d54a-123">Указывает первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="9d54a-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="9d54a-124">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="9d54a-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="9d54a-125">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="9d54a-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="9d54a-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="9d54a-126">-SecondaryKey</span></span>
<span data-ttu-id="9d54a-127">Задает вторичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="9d54a-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="9d54a-128">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="9d54a-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="9d54a-129">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="9d54a-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="9d54a-130">-State</span><span class="sxs-lookup"><span data-stu-id="9d54a-130">-State</span></span>
<span data-ttu-id="9d54a-131">Указывает состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="9d54a-131">Specifies the subscription state.</span></span>
<span data-ttu-id="9d54a-132">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9d54a-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="9d54a-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="9d54a-133">-StateComment</span></span>
<span data-ttu-id="9d54a-134">Указывает Примечание о состоянии подписки.</span><span class="sxs-lookup"><span data-stu-id="9d54a-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="9d54a-135">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9d54a-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="9d54a-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d54a-136">-SubscriptionId</span></span>
<span data-ttu-id="9d54a-137">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="9d54a-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="9d54a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d54a-138">CommonParameters</span></span>
<span data-ttu-id="9d54a-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d54a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d54a-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d54a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d54a-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d54a-141">INPUTS</span></span>

### <span data-ttu-id="9d54a-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9d54a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9d54a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9d54a-143">System.String</span></span>

### <span data-ttu-id="9d54a-144">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="9d54a-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9d54a-145">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9d54a-145">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9d54a-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9d54a-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9d54a-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d54a-147">OUTPUTS</span></span>

### <span data-ttu-id="9d54a-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d54a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="9d54a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d54a-149">NOTES</span></span>

## <span data-ttu-id="9d54a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d54a-150">RELATED LINKS</span></span>

[<span data-ttu-id="9d54a-151">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d54a-151">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9d54a-152">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d54a-152">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9d54a-153">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d54a-153">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


