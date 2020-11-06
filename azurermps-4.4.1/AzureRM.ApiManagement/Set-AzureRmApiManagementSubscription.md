---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559976"
---
# <span data-ttu-id="b58b5-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b58b5-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="b58b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b58b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b58b5-103">Задает сведения о существующем подписке.</span><span class="sxs-lookup"><span data-stu-id="b58b5-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b58b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b58b5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b58b5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b58b5-105">DESCRIPTION</span></span>
<span data-ttu-id="b58b5-106">Командлет **Set-AzureRmApiManagementSubscription** задает существующие сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="b58b5-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="b58b5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b58b5-107">EXAMPLES</span></span>

### <span data-ttu-id="b58b5-108">Пример 1: Настройка состояния и первичных и вторичных ключей для подписки</span><span class="sxs-lookup"><span data-stu-id="b58b5-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="b58b5-109">Эта команда задает первичные и вторичные ключи для подписки и активирует ее.</span><span class="sxs-lookup"><span data-stu-id="b58b5-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="b58b5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b58b5-110">PARAMETERS</span></span>

### <span data-ttu-id="b58b5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b58b5-111">-Context</span></span>
<span data-ttu-id="b58b5-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b58b5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b58b5-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="b58b5-113">-ExpiresOn</span></span>
<span data-ttu-id="b58b5-114">Указывает дату окончания срока действия подписки.</span><span class="sxs-lookup"><span data-stu-id="b58b5-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="b58b5-115">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b58b5-115">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b58b5-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b58b5-116">-Name</span></span>
<span data-ttu-id="b58b5-117">Указывает имя подписки.</span><span class="sxs-lookup"><span data-stu-id="b58b5-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="b58b5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b58b5-118">-PassThru</span></span>
<span data-ttu-id="b58b5-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="b58b5-119">passthru</span></span>

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

### <span data-ttu-id="b58b5-120">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b58b5-120">-PrimaryKey</span></span>
<span data-ttu-id="b58b5-121">Указывает первичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="b58b5-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="b58b5-122">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="b58b5-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="b58b5-123">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="b58b5-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b58b5-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b58b5-124">-SecondaryKey</span></span>
<span data-ttu-id="b58b5-125">Задает вторичный ключ подписки.</span><span class="sxs-lookup"><span data-stu-id="b58b5-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="b58b5-126">Этот параметр создается автоматически, если не указан.</span><span class="sxs-lookup"><span data-stu-id="b58b5-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="b58b5-127">Этот параметр должен содержать от 1 до 300 символов.</span><span class="sxs-lookup"><span data-stu-id="b58b5-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b58b5-128">-State</span><span class="sxs-lookup"><span data-stu-id="b58b5-128">-State</span></span>
<span data-ttu-id="b58b5-129">Указывает состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="b58b5-129">Specifies the subscription state.</span></span>
<span data-ttu-id="b58b5-130">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b58b5-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b58b5-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="b58b5-131">-StateComment</span></span>
<span data-ttu-id="b58b5-132">Указывает Примечание о состоянии подписки.</span><span class="sxs-lookup"><span data-stu-id="b58b5-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="b58b5-133">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b58b5-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b58b5-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b58b5-134">-SubscriptionId</span></span>
<span data-ttu-id="b58b5-135">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="b58b5-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="b58b5-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b58b5-136">-DefaultProfile</span></span>
<span data-ttu-id="b58b5-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b58b5-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b58b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b58b5-138">CommonParameters</span></span>
<span data-ttu-id="b58b5-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b58b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b58b5-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b58b5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b58b5-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b58b5-141">INPUTS</span></span>

## <span data-ttu-id="b58b5-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b58b5-142">OUTPUTS</span></span>

### <span data-ttu-id="b58b5-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="b58b5-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="b58b5-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b58b5-144">NOTES</span></span>

## <span data-ttu-id="b58b5-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b58b5-145">RELATED LINKS</span></span>

[<span data-ttu-id="b58b5-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b58b5-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b58b5-147">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b58b5-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b58b5-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b58b5-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


