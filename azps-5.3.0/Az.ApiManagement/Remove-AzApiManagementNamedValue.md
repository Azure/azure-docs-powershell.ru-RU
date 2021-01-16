---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423372"
---
# <span data-ttu-id="afdff-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="afdff-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="afdff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afdff-102">SYNOPSIS</span></span>
<span data-ttu-id="afdff-103">Удаляет именуемую величину управления API.</span><span class="sxs-lookup"><span data-stu-id="afdff-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="afdff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="afdff-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afdff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afdff-105">DESCRIPTION</span></span>
<span data-ttu-id="afdff-106">Для удаления именуемого значения управления API Azure удаляется cmdlet **Remove-AzApiManagementNamedValue.** </span><span class="sxs-lookup"><span data-stu-id="afdff-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="afdff-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="afdff-107">EXAMPLES</span></span>

### <span data-ttu-id="afdff-108">Пример 1. Удаление именоваемой величины</span><span class="sxs-lookup"><span data-stu-id="afdff-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="afdff-109">Эта команда удаляет именуемую величину, у которого есть свойство ID Property11.</span><span class="sxs-lookup"><span data-stu-id="afdff-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="afdff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afdff-110">PARAMETERS</span></span>

### <span data-ttu-id="afdff-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="afdff-111">-Context</span></span>
<span data-ttu-id="afdff-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="afdff-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="afdff-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="afdff-113">This parameter is required.</span></span>

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

### <span data-ttu-id="afdff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afdff-114">-DefaultProfile</span></span>
<span data-ttu-id="afdff-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afdff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afdff-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="afdff-116">-NamedValueId</span></span>
<span data-ttu-id="afdff-117">Идентификатор существующего именоваемого значения.</span><span class="sxs-lookup"><span data-stu-id="afdff-117">Identifier of existing named value.</span></span>
<span data-ttu-id="afdff-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="afdff-118">This parameter is required.</span></span>

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

### <span data-ttu-id="afdff-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afdff-119">-PassThru</span></span>
<span data-ttu-id="afdff-120">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="afdff-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="afdff-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="afdff-121">This parameter is optional.</span></span>
<span data-ttu-id="afdff-122">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="afdff-122">Default value is false.</span></span>

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

### <span data-ttu-id="afdff-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afdff-123">-Confirm</span></span>
<span data-ttu-id="afdff-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afdff-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afdff-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afdff-125">-WhatIf</span></span>
<span data-ttu-id="afdff-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afdff-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afdff-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="afdff-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afdff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afdff-128">CommonParameters</span></span>
<span data-ttu-id="afdff-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afdff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afdff-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afdff-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afdff-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afdff-131">INPUTS</span></span>

### <span data-ttu-id="afdff-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="afdff-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="afdff-133">System.String</span><span class="sxs-lookup"><span data-stu-id="afdff-133">System.String</span></span>

### <span data-ttu-id="afdff-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="afdff-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="afdff-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afdff-135">OUTPUTS</span></span>

### <span data-ttu-id="afdff-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="afdff-136">System.Boolean</span></span>

## <span data-ttu-id="afdff-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="afdff-137">NOTES</span></span>

## <span data-ttu-id="afdff-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afdff-138">RELATED LINKS</span></span>