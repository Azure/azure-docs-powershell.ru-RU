---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 72dbe137fd783cb8941fe27e6883bd0ed8e08206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901646"
---
# <span data-ttu-id="9057c-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9057c-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="9057c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9057c-102">SYNOPSIS</span></span>
<span data-ttu-id="9057c-103">Удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="9057c-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="9057c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9057c-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9057c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9057c-105">DESCRIPTION</span></span>
<span data-ttu-id="9057c-106">Командлет **Remove-AzApiManagementProduct** удаляет существующий продукт для управления API.</span><span class="sxs-lookup"><span data-stu-id="9057c-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="9057c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9057c-107">EXAMPLES</span></span>

### <span data-ttu-id="9057c-108">Пример 1: удаление существующего продукта и всех подписок</span><span class="sxs-lookup"><span data-stu-id="9057c-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="9057c-109">Эта команда удаляет существующий продукт и все подписки.</span><span class="sxs-lookup"><span data-stu-id="9057c-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="9057c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9057c-110">PARAMETERS</span></span>

### <span data-ttu-id="9057c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9057c-111">-Context</span></span>
<span data-ttu-id="9057c-112">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9057c-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9057c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9057c-113">-DefaultProfile</span></span>
<span data-ttu-id="9057c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9057c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9057c-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="9057c-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="9057c-116">Указывает, нужно ли удалять подписку на продукт.</span><span class="sxs-lookup"><span data-stu-id="9057c-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="9057c-117">Если вы не настроили этот параметр и подписки уже существуют, создается исключение.</span><span class="sxs-lookup"><span data-stu-id="9057c-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="9057c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9057c-118">-PassThru</span></span>
<span data-ttu-id="9057c-119">Указывает на то, что этот командлет возвращает значение $True, если оно завершается успешно, или значение $False, если оно завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="9057c-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="9057c-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9057c-120">-ProductId</span></span>
<span data-ttu-id="9057c-121">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="9057c-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="9057c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9057c-122">-Confirm</span></span>
<span data-ttu-id="9057c-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9057c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9057c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9057c-124">-WhatIf</span></span>
<span data-ttu-id="9057c-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9057c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9057c-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9057c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9057c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9057c-127">CommonParameters</span></span>
<span data-ttu-id="9057c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9057c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9057c-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9057c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9057c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9057c-130">INPUTS</span></span>

### <span data-ttu-id="9057c-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9057c-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9057c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9057c-132">System.String</span></span>

### <span data-ttu-id="9057c-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9057c-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9057c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9057c-134">OUTPUTS</span></span>

### <span data-ttu-id="9057c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9057c-135">System.Boolean</span></span>

## <span data-ttu-id="9057c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9057c-136">NOTES</span></span>

## <span data-ttu-id="9057c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9057c-137">RELATED LINKS</span></span>

[<span data-ttu-id="9057c-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9057c-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="9057c-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9057c-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="9057c-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9057c-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


