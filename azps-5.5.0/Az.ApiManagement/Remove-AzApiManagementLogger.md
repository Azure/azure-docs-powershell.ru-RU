---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: e68fec8bf38dc990737f11d5dc3ed079d71fd6ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212108"
---
# <span data-ttu-id="6930e-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6930e-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="6930e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6930e-102">SYNOPSIS</span></span>
<span data-ttu-id="6930e-103">Удаляет журнал управления API.</span><span class="sxs-lookup"><span data-stu-id="6930e-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="6930e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6930e-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6930e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6930e-105">DESCRIPTION</span></span>
<span data-ttu-id="6930e-106">Для удаления журнала управления API Azure **удаляется cmdlet Remove-AzApiManagementLogger.** </span><span class="sxs-lookup"><span data-stu-id="6930e-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="6930e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6930e-107">EXAMPLES</span></span>

### <span data-ttu-id="6930e-108">Пример 1. Удаление регистратора</span><span class="sxs-lookup"><span data-stu-id="6930e-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="6930e-109">Эта команда удаляет регистратор с ИД 123.</span><span class="sxs-lookup"><span data-stu-id="6930e-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="6930e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6930e-110">PARAMETERS</span></span>

### <span data-ttu-id="6930e-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6930e-111">-Context</span></span>
<span data-ttu-id="6930e-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="6930e-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6930e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6930e-113">-DefaultProfile</span></span>
<span data-ttu-id="6930e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6930e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6930e-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="6930e-115">-LoggerId</span></span>
<span data-ttu-id="6930e-116">Определяет ИД регистратора, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6930e-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="6930e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6930e-117">-PassThru</span></span>
<span data-ttu-id="6930e-118">Указывает на то, что этот $True возвращает значение $True успешно или $False противном случае.</span><span class="sxs-lookup"><span data-stu-id="6930e-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="6930e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6930e-119">-Confirm</span></span>
<span data-ttu-id="6930e-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6930e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6930e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6930e-121">-WhatIf</span></span>
<span data-ttu-id="6930e-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6930e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6930e-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6930e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6930e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6930e-124">CommonParameters</span></span>
<span data-ttu-id="6930e-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6930e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6930e-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6930e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6930e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6930e-127">INPUTS</span></span>

### <span data-ttu-id="6930e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6930e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6930e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6930e-129">System.String</span></span>

### <span data-ttu-id="6930e-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6930e-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6930e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6930e-131">OUTPUTS</span></span>

### <span data-ttu-id="6930e-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6930e-132">System.Boolean</span></span>

## <span data-ttu-id="6930e-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6930e-133">NOTES</span></span>

## <span data-ttu-id="6930e-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6930e-134">RELATED LINKS</span></span>

[<span data-ttu-id="6930e-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6930e-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="6930e-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6930e-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="6930e-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6930e-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


