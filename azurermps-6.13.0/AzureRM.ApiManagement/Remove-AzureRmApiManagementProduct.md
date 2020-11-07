---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 61a4ab9e7a827cffce861cc9ebaf7382e16e8fcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732330"
---
# <span data-ttu-id="f4826-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f4826-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="f4826-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4826-102">SYNOPSIS</span></span>
<span data-ttu-id="f4826-103">Удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="f4826-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4826-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4826-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4826-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4826-105">DESCRIPTION</span></span>
<span data-ttu-id="f4826-106">Командлет **Remove-AzureRmApiManagementProduct** удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="f4826-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="f4826-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4826-107">EXAMPLES</span></span>

### <span data-ttu-id="f4826-108">Пример 1: удаление существующего продукта и всех подписок</span><span class="sxs-lookup"><span data-stu-id="f4826-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="f4826-109">Эта команда удаляет существующий продукт и все подписки.</span><span class="sxs-lookup"><span data-stu-id="f4826-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="f4826-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4826-110">PARAMETERS</span></span>

### <span data-ttu-id="f4826-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f4826-111">-Context</span></span>
<span data-ttu-id="f4826-112">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f4826-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f4826-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4826-113">-DefaultProfile</span></span>
<span data-ttu-id="f4826-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4826-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4826-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="f4826-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="f4826-116">Указывает, нужно ли удалять подписку на продукт.</span><span class="sxs-lookup"><span data-stu-id="f4826-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="f4826-117">Если вы не настроили этот параметр и подписки уже существуют, создается исключение.</span><span class="sxs-lookup"><span data-stu-id="f4826-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="f4826-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4826-118">-PassThru</span></span>
<span data-ttu-id="f4826-119">Указывает на то, что этот командлет возвращает значение $True, если оно завершается успешно, или значение $False, если оно завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="f4826-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="f4826-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f4826-120">-ProductId</span></span>
<span data-ttu-id="f4826-121">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="f4826-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="f4826-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4826-122">-Confirm</span></span>
<span data-ttu-id="f4826-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4826-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4826-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4826-124">-WhatIf</span></span>
<span data-ttu-id="f4826-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4826-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4826-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4826-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4826-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4826-127">CommonParameters</span></span>
<span data-ttu-id="f4826-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4826-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4826-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4826-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4826-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4826-130">INPUTS</span></span>

### <span data-ttu-id="f4826-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f4826-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f4826-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4826-132">System.String</span></span>

### <span data-ttu-id="f4826-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4826-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4826-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4826-134">OUTPUTS</span></span>

### <span data-ttu-id="f4826-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4826-135">System.Boolean</span></span>

## <span data-ttu-id="f4826-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4826-136">NOTES</span></span>

## <span data-ttu-id="f4826-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4826-137">RELATED LINKS</span></span>

[<span data-ttu-id="f4826-138">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f4826-138">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="f4826-139">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f4826-139">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="f4826-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f4826-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


