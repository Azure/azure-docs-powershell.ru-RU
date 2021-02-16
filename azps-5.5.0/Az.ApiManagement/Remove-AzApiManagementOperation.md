---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229420"
---
# <span data-ttu-id="45fde-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="45fde-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="45fde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45fde-102">SYNOPSIS</span></span>
<span data-ttu-id="45fde-103">Удаляет существующую операцию.</span><span class="sxs-lookup"><span data-stu-id="45fde-103">Removes an existing operation.</span></span>

## <span data-ttu-id="45fde-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45fde-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45fde-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45fde-105">DESCRIPTION</span></span>
<span data-ttu-id="45fde-106">Для удаления существующей операции будет отключена операция **Remove-AzApiManagementOperation.**</span><span class="sxs-lookup"><span data-stu-id="45fde-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="45fde-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45fde-107">EXAMPLES</span></span>

### <span data-ttu-id="45fde-108">Пример 1. Удаление существующей операции API</span><span class="sxs-lookup"><span data-stu-id="45fde-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="45fde-109">Эта команда удаляет существующую операцию API.</span><span class="sxs-lookup"><span data-stu-id="45fde-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="45fde-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45fde-110">PARAMETERS</span></span>

### <span data-ttu-id="45fde-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="45fde-111">-ApiId</span></span>
<span data-ttu-id="45fde-112">Определяет идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="45fde-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="45fde-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="45fde-113">-ApiRevision</span></span>
<span data-ttu-id="45fde-114">Идентификатор изменения API.</span><span class="sxs-lookup"><span data-stu-id="45fde-114">Identifier of API Revision.</span></span> <span data-ttu-id="45fde-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="45fde-115">This parameter is optional.</span></span> <span data-ttu-id="45fde-116">Если не указано, операция будет удалена из активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="45fde-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="45fde-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="45fde-117">-Context</span></span>
<span data-ttu-id="45fde-118">Указывает экземпляр **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="45fde-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="45fde-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fde-119">-DefaultProfile</span></span>
<span data-ttu-id="45fde-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45fde-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45fde-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="45fde-121">-OperationId</span></span>
<span data-ttu-id="45fde-122">Определяет идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="45fde-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="45fde-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45fde-123">-PassThru</span></span>
<span data-ttu-id="45fde-124">Указывает на то, что этот $True возвращает значение, если он успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="45fde-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="45fde-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45fde-125">-Confirm</span></span>
<span data-ttu-id="45fde-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45fde-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45fde-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45fde-127">-WhatIf</span></span>
<span data-ttu-id="45fde-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45fde-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45fde-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45fde-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45fde-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fde-130">CommonParameters</span></span>
<span data-ttu-id="45fde-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45fde-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fde-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45fde-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fde-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45fde-133">INPUTS</span></span>

### <span data-ttu-id="45fde-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="45fde-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45fde-135">System.String</span><span class="sxs-lookup"><span data-stu-id="45fde-135">System.String</span></span>

### <span data-ttu-id="45fde-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45fde-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45fde-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45fde-137">OUTPUTS</span></span>

### <span data-ttu-id="45fde-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45fde-138">System.Boolean</span></span>

## <span data-ttu-id="45fde-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45fde-139">NOTES</span></span>

## <span data-ttu-id="45fde-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45fde-140">RELATED LINKS</span></span>

[<span data-ttu-id="45fde-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="45fde-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="45fde-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="45fde-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="45fde-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="45fde-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


