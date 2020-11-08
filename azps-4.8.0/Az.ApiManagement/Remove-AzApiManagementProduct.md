---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079858"
---
# <span data-ttu-id="1803b-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1803b-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="1803b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1803b-102">SYNOPSIS</span></span>
<span data-ttu-id="1803b-103">Удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="1803b-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="1803b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1803b-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1803b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1803b-105">DESCRIPTION</span></span>
<span data-ttu-id="1803b-106">Командлет **Remove-AzApiManagementProduct** удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="1803b-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="1803b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1803b-107">EXAMPLES</span></span>

### <span data-ttu-id="1803b-108">Пример 1: удаление существующего продукта и всех подписок</span><span class="sxs-lookup"><span data-stu-id="1803b-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="1803b-109">Эта команда удаляет существующий продукт и все подписки.</span><span class="sxs-lookup"><span data-stu-id="1803b-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="1803b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1803b-110">PARAMETERS</span></span>

### <span data-ttu-id="1803b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1803b-111">-Context</span></span>
<span data-ttu-id="1803b-112">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1803b-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1803b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1803b-113">-DefaultProfile</span></span>
<span data-ttu-id="1803b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1803b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1803b-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="1803b-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="1803b-116">Указывает, нужно ли удалять подписку на продукт.</span><span class="sxs-lookup"><span data-stu-id="1803b-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="1803b-117">Если вы не настроили этот параметр и подписки уже существуют, создается исключение.</span><span class="sxs-lookup"><span data-stu-id="1803b-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="1803b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1803b-118">-PassThru</span></span>
<span data-ttu-id="1803b-119">Указывает на то, что этот командлет возвращает значение $True, если оно завершается успешно, или значение $False, если оно завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="1803b-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="1803b-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1803b-120">-ProductId</span></span>
<span data-ttu-id="1803b-121">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="1803b-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="1803b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1803b-122">-Confirm</span></span>
<span data-ttu-id="1803b-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1803b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1803b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1803b-124">-WhatIf</span></span>
<span data-ttu-id="1803b-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1803b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1803b-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1803b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1803b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1803b-127">CommonParameters</span></span>
<span data-ttu-id="1803b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1803b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1803b-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1803b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1803b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1803b-130">INPUTS</span></span>

### <span data-ttu-id="1803b-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1803b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1803b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1803b-132">System.String</span></span>

### <span data-ttu-id="1803b-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1803b-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1803b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1803b-134">OUTPUTS</span></span>

### <span data-ttu-id="1803b-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1803b-135">System.Boolean</span></span>

## <span data-ttu-id="1803b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1803b-136">NOTES</span></span>

## <span data-ttu-id="1803b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1803b-137">RELATED LINKS</span></span>

[<span data-ttu-id="1803b-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1803b-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="1803b-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1803b-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="1803b-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1803b-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


