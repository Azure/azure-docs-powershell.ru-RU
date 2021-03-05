---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 9ad08f867bf78dc4a6bc2df5c4dd3086c3cea33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979027"
---
# <span data-ttu-id="cad80-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cad80-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="cad80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cad80-102">SYNOPSIS</span></span>
<span data-ttu-id="cad80-103">Удаляет существующий продукт управления API.</span><span class="sxs-lookup"><span data-stu-id="cad80-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="cad80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cad80-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad80-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cad80-105">DESCRIPTION</span></span>
<span data-ttu-id="cad80-106">Для удаления существующего продукта управления API будет удаляем существующий **cmdlet AzApiManagementProduct.**</span><span class="sxs-lookup"><span data-stu-id="cad80-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="cad80-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cad80-107">EXAMPLES</span></span>

### <span data-ttu-id="cad80-108">Пример 1. Удаление существующего продукта и всех подписок</span><span class="sxs-lookup"><span data-stu-id="cad80-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="cad80-109">Эта команда удаляет существующий продукт и все подписки.</span><span class="sxs-lookup"><span data-stu-id="cad80-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="cad80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cad80-110">PARAMETERS</span></span>

### <span data-ttu-id="cad80-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="cad80-111">-Context</span></span>
<span data-ttu-id="cad80-112">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="cad80-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cad80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad80-113">-DefaultProfile</span></span>
<span data-ttu-id="cad80-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cad80-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cad80-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="cad80-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="cad80-116">Указывает, нужно ли удалять подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="cad80-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="cad80-117">Если этот параметр не задан и подписки существуют, вы имеете исключение.</span><span class="sxs-lookup"><span data-stu-id="cad80-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="cad80-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cad80-118">-PassThru</span></span>
<span data-ttu-id="cad80-119">Указывает на то, что этот $True возвращает значение $True, если он успешно, или значение $False в случае сбой.</span><span class="sxs-lookup"><span data-stu-id="cad80-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="cad80-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cad80-120">-ProductId</span></span>
<span data-ttu-id="cad80-121">Определяет идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="cad80-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="cad80-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cad80-122">-Confirm</span></span>
<span data-ttu-id="cad80-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cad80-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad80-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad80-124">-WhatIf</span></span>
<span data-ttu-id="cad80-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cad80-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cad80-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cad80-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad80-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad80-127">CommonParameters</span></span>
<span data-ttu-id="cad80-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cad80-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad80-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cad80-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad80-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cad80-130">INPUTS</span></span>

### <span data-ttu-id="cad80-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cad80-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cad80-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cad80-132">System.String</span></span>

### <span data-ttu-id="cad80-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cad80-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cad80-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cad80-134">OUTPUTS</span></span>

### <span data-ttu-id="cad80-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cad80-135">System.Boolean</span></span>

## <span data-ttu-id="cad80-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cad80-136">NOTES</span></span>

## <span data-ttu-id="cad80-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cad80-137">RELATED LINKS</span></span>

[<span data-ttu-id="cad80-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cad80-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="cad80-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cad80-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="cad80-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="cad80-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


