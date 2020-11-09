---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319376"
---
# <span data-ttu-id="2b2fa-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2b2fa-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="2b2fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2fa-103">Удаляет именованное значение для управления API.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="2b2fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b2fa-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b2fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b2fa-105">DESCRIPTION</span></span>
<span data-ttu-id="2b2fa-106">Командлет **Remove-AzApiManagementNamedValue** удаляет **именованное значение** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="2b2fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b2fa-107">EXAMPLES</span></span>

### <span data-ttu-id="2b2fa-108">Пример 1: удаление именованного значения</span><span class="sxs-lookup"><span data-stu-id="2b2fa-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="2b2fa-109">Эта команда удаляет именованное значение с ИДЕНТИФИКАТОРом Property11.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="2b2fa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b2fa-110">PARAMETERS</span></span>

### <span data-ttu-id="2b2fa-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2b2fa-111">-Context</span></span>
<span data-ttu-id="2b2fa-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2b2fa-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2b2fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2fa-114">-DefaultProfile</span></span>
<span data-ttu-id="2b2fa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b2fa-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="2b2fa-116">-NamedValueId</span></span>
<span data-ttu-id="2b2fa-117">Идентификатор существующего именованного значения.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-117">Identifier of existing named value.</span></span>
<span data-ttu-id="2b2fa-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2b2fa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b2fa-119">-PassThru</span></span>
<span data-ttu-id="2b2fa-120">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2b2fa-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-121">This parameter is optional.</span></span>
<span data-ttu-id="2b2fa-122">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-122">Default value is false.</span></span>

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

### <span data-ttu-id="2b2fa-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b2fa-123">-Confirm</span></span>
<span data-ttu-id="2b2fa-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b2fa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b2fa-125">-WhatIf</span></span>
<span data-ttu-id="2b2fa-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b2fa-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b2fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2fa-128">CommonParameters</span></span>
<span data-ttu-id="2b2fa-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2fa-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b2fa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2fa-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b2fa-131">INPUTS</span></span>

### <span data-ttu-id="2b2fa-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b2fa-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b2fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2b2fa-133">System.String</span></span>

### <span data-ttu-id="2b2fa-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b2fa-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2b2fa-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b2fa-135">OUTPUTS</span></span>

### <span data-ttu-id="2b2fa-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b2fa-136">System.Boolean</span></span>

## <span data-ttu-id="2b2fa-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b2fa-137">NOTES</span></span>

## <span data-ttu-id="2b2fa-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b2fa-138">RELATED LINKS</span></span>
