---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: 3101f58720130a6e5f7c91fb4489d96915d8c4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957827"
---
# <span data-ttu-id="6ab5e-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="6ab5e-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="6ab5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab5e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab5e-103">Удаляет именуемую величину управления API.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="6ab5e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ab5e-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ab5e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ab5e-105">DESCRIPTION</span></span>
<span data-ttu-id="6ab5e-106">Для удаления именуемого значения управления API Azure удаляется значение  **Remove-AzApiManagementNamedValue.**</span><span class="sxs-lookup"><span data-stu-id="6ab5e-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="6ab5e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ab5e-107">EXAMPLES</span></span>

### <span data-ttu-id="6ab5e-108">Пример 1. Удаление именоваемой величины</span><span class="sxs-lookup"><span data-stu-id="6ab5e-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="6ab5e-109">Эта команда удаляет именуемую величину, у которого есть свойство ID Property11.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="6ab5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ab5e-110">PARAMETERS</span></span>

### <span data-ttu-id="6ab5e-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6ab5e-111">-Context</span></span>
<span data-ttu-id="6ab5e-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6ab5e-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6ab5e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6ab5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab5e-114">-DefaultProfile</span></span>
<span data-ttu-id="6ab5e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab5e-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="6ab5e-116">-NamedValueId</span></span>
<span data-ttu-id="6ab5e-117">Идентификатор существующего именоваемого значения.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-117">Identifier of existing named value.</span></span>
<span data-ttu-id="6ab5e-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6ab5e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6ab5e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ab5e-119">-PassThru</span></span>
<span data-ttu-id="6ab5e-120">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6ab5e-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-121">This parameter is optional.</span></span>
<span data-ttu-id="6ab5e-122">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-122">Default value is false.</span></span>

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

### <span data-ttu-id="6ab5e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ab5e-123">-Confirm</span></span>
<span data-ttu-id="6ab5e-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab5e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab5e-125">-WhatIf</span></span>
<span data-ttu-id="6ab5e-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ab5e-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab5e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab5e-128">CommonParameters</span></span>
<span data-ttu-id="6ab5e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab5e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab5e-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ab5e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab5e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ab5e-131">INPUTS</span></span>

### <span data-ttu-id="6ab5e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6ab5e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6ab5e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6ab5e-133">System.String</span></span>

### <span data-ttu-id="6ab5e-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ab5e-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6ab5e-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ab5e-135">OUTPUTS</span></span>

### <span data-ttu-id="6ab5e-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ab5e-136">System.Boolean</span></span>

## <span data-ttu-id="6ab5e-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ab5e-137">NOTES</span></span>

## <span data-ttu-id="6ab5e-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ab5e-138">RELATED LINKS</span></span>
