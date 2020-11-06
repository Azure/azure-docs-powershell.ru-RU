---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 505a26c48e53fe05e8724d61d5ddb66981e87ee9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558007"
---
# <span data-ttu-id="16c79-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="16c79-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="16c79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16c79-102">SYNOPSIS</span></span>
<span data-ttu-id="16c79-103">Удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="16c79-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16c79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16c79-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16c79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c79-105">DESCRIPTION</span></span>
<span data-ttu-id="16c79-106">Командлет **Remove-AzureRmApiManagementProduct** удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="16c79-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="16c79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16c79-107">EXAMPLES</span></span>

### <span data-ttu-id="16c79-108">Пример 1: удаление существующего продукта и всех подписок</span><span class="sxs-lookup"><span data-stu-id="16c79-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>Remove-AzureRmApiManagementProduct -Context $APImContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="16c79-109">Эта команда удаляет существующий продукт и все подписки.</span><span class="sxs-lookup"><span data-stu-id="16c79-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="16c79-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16c79-110">PARAMETERS</span></span>

### <span data-ttu-id="16c79-111">-Context</span><span class="sxs-lookup"><span data-stu-id="16c79-111">-Context</span></span>
<span data-ttu-id="16c79-112">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="16c79-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="16c79-113">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="16c79-113">-DeleteSubscriptions</span></span>
<span data-ttu-id="16c79-114">Указывает, нужно ли удалять подписку на продукт.</span><span class="sxs-lookup"><span data-stu-id="16c79-114">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="16c79-115">Если вы не настроили этот параметр и подписки уже существуют, создается исключение.</span><span class="sxs-lookup"><span data-stu-id="16c79-115">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="16c79-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16c79-116">-PassThru</span></span>
<span data-ttu-id="16c79-117">Указывает на то, что этот командлет возвращает значение $True, если оно завершается успешно, или значение $False, если оно завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="16c79-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="16c79-118">-ProductId</span><span class="sxs-lookup"><span data-stu-id="16c79-118">-ProductId</span></span>
<span data-ttu-id="16c79-119">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="16c79-119">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="16c79-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16c79-120">-Confirm</span></span>
<span data-ttu-id="16c79-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16c79-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c79-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c79-122">-WhatIf</span></span>
<span data-ttu-id="16c79-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16c79-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c79-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16c79-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c79-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c79-125">-DefaultProfile</span></span>
<span data-ttu-id="16c79-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16c79-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16c79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c79-127">CommonParameters</span></span>
<span data-ttu-id="16c79-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16c79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c79-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16c79-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c79-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16c79-130">INPUTS</span></span>

## <span data-ttu-id="16c79-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c79-131">OUTPUTS</span></span>

### <span data-ttu-id="16c79-132">логических</span><span class="sxs-lookup"><span data-stu-id="16c79-132">bool</span></span>

## <span data-ttu-id="16c79-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="16c79-133">NOTES</span></span>

## <span data-ttu-id="16c79-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16c79-134">RELATED LINKS</span></span>

[<span data-ttu-id="16c79-135">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="16c79-135">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="16c79-136">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="16c79-136">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="16c79-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="16c79-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


