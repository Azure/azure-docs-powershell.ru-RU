---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392220"
---
# <span data-ttu-id="7caed-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7caed-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="7caed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7caed-102">SYNOPSIS</span></span>
<span data-ttu-id="7caed-103">Удаляет существующий продукт управления API.</span><span class="sxs-lookup"><span data-stu-id="7caed-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="7caed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7caed-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7caed-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7caed-105">DESCRIPTION</span></span>
<span data-ttu-id="7caed-106">Для удаления существующего продукта управления API будет удаляем **существующий cmdlet Remove-AzApiManagementProduct.**</span><span class="sxs-lookup"><span data-stu-id="7caed-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="7caed-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7caed-107">EXAMPLES</span></span>

### <span data-ttu-id="7caed-108">Пример 1. Удаление существующего продукта и всех подписок</span><span class="sxs-lookup"><span data-stu-id="7caed-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="7caed-109">Эта команда удаляет существующий продукт и все подписки.</span><span class="sxs-lookup"><span data-stu-id="7caed-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="7caed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7caed-110">PARAMETERS</span></span>

### <span data-ttu-id="7caed-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="7caed-111">-Context</span></span>
<span data-ttu-id="7caed-112">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="7caed-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7caed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7caed-113">-DefaultProfile</span></span>
<span data-ttu-id="7caed-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7caed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7caed-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="7caed-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="7caed-116">Указывает, нужно ли удалять подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="7caed-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="7caed-117">Если этот параметр не задан и подписки существуют, высылается исключение.</span><span class="sxs-lookup"><span data-stu-id="7caed-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="7caed-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7caed-118">-PassThru</span></span>
<span data-ttu-id="7caed-119">Указывает на то, что этот $True возвращает значение $True, если он успешно, или значение $False в случае сбой.</span><span class="sxs-lookup"><span data-stu-id="7caed-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="7caed-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7caed-120">-ProductId</span></span>
<span data-ttu-id="7caed-121">Определяет идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="7caed-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="7caed-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7caed-122">-Confirm</span></span>
<span data-ttu-id="7caed-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7caed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7caed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7caed-124">-WhatIf</span></span>
<span data-ttu-id="7caed-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7caed-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7caed-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7caed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7caed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7caed-127">CommonParameters</span></span>
<span data-ttu-id="7caed-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7caed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7caed-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7caed-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7caed-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7caed-130">INPUTS</span></span>

### <span data-ttu-id="7caed-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7caed-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7caed-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7caed-132">System.String</span></span>

### <span data-ttu-id="7caed-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7caed-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7caed-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7caed-134">OUTPUTS</span></span>

### <span data-ttu-id="7caed-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7caed-135">System.Boolean</span></span>

## <span data-ttu-id="7caed-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7caed-136">NOTES</span></span>

## <span data-ttu-id="7caed-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7caed-137">RELATED LINKS</span></span>

[<span data-ttu-id="7caed-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7caed-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="7caed-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7caed-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="7caed-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7caed-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


