---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 777d71dec17f75cba84c15c7499e5ec56ffb854a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735125"
---
# <span data-ttu-id="9d158-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d158-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="9d158-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d158-102">SYNOPSIS</span></span>
<span data-ttu-id="9d158-103">Удаление существующей подписки.</span><span class="sxs-lookup"><span data-stu-id="9d158-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d158-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d158-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d158-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d158-105">DESCRIPTION</span></span>
<span data-ttu-id="9d158-106">Командлет **Remove-AzureRmApiManagementSubscription** удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="9d158-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="9d158-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d158-107">EXAMPLES</span></span>

### <span data-ttu-id="9d158-108">Пример 1: Удаление подписки</span><span class="sxs-lookup"><span data-stu-id="9d158-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="9d158-109">Эта команда удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="9d158-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="9d158-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d158-110">PARAMETERS</span></span>

### <span data-ttu-id="9d158-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9d158-111">-Context</span></span>
<span data-ttu-id="9d158-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9d158-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d158-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d158-113">-DefaultProfile</span></span>
<span data-ttu-id="9d158-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d158-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d158-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d158-115">-PassThru</span></span>
<span data-ttu-id="9d158-116">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $false, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9d158-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d158-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d158-117">-SubscriptionId</span></span>
<span data-ttu-id="9d158-118">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="9d158-118">Specifies the subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d158-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d158-119">-Confirm</span></span>
<span data-ttu-id="9d158-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d158-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d158-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d158-121">-WhatIf</span></span>
<span data-ttu-id="9d158-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9d158-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d158-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9d158-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d158-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d158-124">CommonParameters</span></span>
<span data-ttu-id="9d158-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d158-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d158-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d158-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d158-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d158-127">INPUTS</span></span>

### <span data-ttu-id="9d158-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="9d158-128">None</span></span>
<span data-ttu-id="9d158-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9d158-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d158-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d158-130">OUTPUTS</span></span>

### <span data-ttu-id="9d158-131">Значением</span><span class="sxs-lookup"><span data-stu-id="9d158-131">Boolean</span></span>

## <span data-ttu-id="9d158-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d158-132">NOTES</span></span>

## <span data-ttu-id="9d158-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d158-133">RELATED LINKS</span></span>

[<span data-ttu-id="9d158-134">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d158-134">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9d158-135">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d158-135">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9d158-136">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9d158-136">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


