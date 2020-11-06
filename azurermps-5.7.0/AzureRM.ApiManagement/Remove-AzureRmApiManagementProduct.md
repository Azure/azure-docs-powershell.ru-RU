---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557628"
---
# <span data-ttu-id="ab63f-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab63f-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="ab63f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab63f-102">SYNOPSIS</span></span>
<span data-ttu-id="ab63f-103">Удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="ab63f-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab63f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab63f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab63f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab63f-105">DESCRIPTION</span></span>
<span data-ttu-id="ab63f-106">Командлет **Remove-AzureRmApiManagementProduct** удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="ab63f-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="ab63f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab63f-107">EXAMPLES</span></span>

### <span data-ttu-id="ab63f-108">Пример 1: удаление существующего продукта и всех подписок</span><span class="sxs-lookup"><span data-stu-id="ab63f-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="ab63f-109">Эта команда удаляет существующий продукт и все подписки.</span><span class="sxs-lookup"><span data-stu-id="ab63f-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="ab63f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab63f-110">PARAMETERS</span></span>

### <span data-ttu-id="ab63f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ab63f-111">-Context</span></span>
<span data-ttu-id="ab63f-112">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ab63f-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ab63f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab63f-113">-DefaultProfile</span></span>
<span data-ttu-id="ab63f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab63f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ab63f-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="ab63f-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="ab63f-116">Указывает, нужно ли удалять подписку на продукт.</span><span class="sxs-lookup"><span data-stu-id="ab63f-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="ab63f-117">Если вы не настроили этот параметр и подписки уже существуют, создается исключение.</span><span class="sxs-lookup"><span data-stu-id="ab63f-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="ab63f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab63f-118">-PassThru</span></span>
<span data-ttu-id="ab63f-119">Указывает на то, что этот командлет возвращает значение $True, если оно завершается успешно, или значение $False, если оно завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="ab63f-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="ab63f-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ab63f-120">-ProductId</span></span>
<span data-ttu-id="ab63f-121">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="ab63f-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="ab63f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab63f-122">-Confirm</span></span>
<span data-ttu-id="ab63f-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ab63f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab63f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab63f-124">-WhatIf</span></span>
<span data-ttu-id="ab63f-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ab63f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab63f-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ab63f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab63f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab63f-127">CommonParameters</span></span>
<span data-ttu-id="ab63f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab63f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab63f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab63f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab63f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab63f-130">INPUTS</span></span>

### <span data-ttu-id="ab63f-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="ab63f-131">None</span></span>
<span data-ttu-id="ab63f-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ab63f-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab63f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab63f-133">OUTPUTS</span></span>

### <span data-ttu-id="ab63f-134">логических</span><span class="sxs-lookup"><span data-stu-id="ab63f-134">bool</span></span>

## <span data-ttu-id="ab63f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab63f-135">NOTES</span></span>

## <span data-ttu-id="ab63f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab63f-136">RELATED LINKS</span></span>

[<span data-ttu-id="ab63f-137">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab63f-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="ab63f-138">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab63f-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="ab63f-139">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ab63f-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


