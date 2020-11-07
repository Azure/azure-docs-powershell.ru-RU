---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: 4fa05a0c3568d8d787a7b269cd0f26c0adc82d0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728000"
---
# <span data-ttu-id="05ad3-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="05ad3-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="05ad3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="05ad3-103">Удаляет схему API из API.</span><span class="sxs-lookup"><span data-stu-id="05ad3-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="05ad3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05ad3-104">SYNTAX</span></span>

### <span data-ttu-id="05ad3-105">ByApiSchemaId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05ad3-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05ad3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05ad3-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05ad3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05ad3-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ad3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05ad3-108">DESCRIPTION</span></span>
<span data-ttu-id="05ad3-109">Командлет **Remove-AzApiManagementSchema** из API.</span><span class="sxs-lookup"><span data-stu-id="05ad3-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="05ad3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05ad3-110">EXAMPLES</span></span>

### <span data-ttu-id="05ad3-111">Пример 1: удаление схемы API из API</span><span class="sxs-lookup"><span data-stu-id="05ad3-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="05ad3-112">Сценарий удаляет схему `2` из API, `echo-api` если она не указана.</span><span class="sxs-lookup"><span data-stu-id="05ad3-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="05ad3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05ad3-113">PARAMETERS</span></span>

### <span data-ttu-id="05ad3-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="05ad3-114">-ApiId</span></span>
<span data-ttu-id="05ad3-115">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="05ad3-115">Identifier of the API.</span></span>
<span data-ttu-id="05ad3-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="05ad3-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ad3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="05ad3-117">-Context</span></span>
<span data-ttu-id="05ad3-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="05ad3-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="05ad3-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="05ad3-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ad3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ad3-120">-DefaultProfile</span></span>
<span data-ttu-id="05ad3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05ad3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05ad3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05ad3-122">-InputObject</span></span>
<span data-ttu-id="05ad3-123">Экземпляр PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="05ad3-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="05ad3-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="05ad3-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ad3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05ad3-125">-PassThru</span></span>
<span data-ttu-id="05ad3-126">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="05ad3-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="05ad3-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="05ad3-127">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ad3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05ad3-128">-ResourceId</span></span>
<span data-ttu-id="05ad3-129">ИД ResourceId для ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="05ad3-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="05ad3-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="05ad3-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ad3-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="05ad3-131">-SchemaId</span></span>
<span data-ttu-id="05ad3-132">Идентификатор схемы API.</span><span class="sxs-lookup"><span data-stu-id="05ad3-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="05ad3-133">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="05ad3-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ad3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05ad3-134">-Confirm</span></span>
<span data-ttu-id="05ad3-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05ad3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ad3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ad3-136">-WhatIf</span></span>
<span data-ttu-id="05ad3-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05ad3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ad3-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05ad3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ad3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ad3-139">CommonParameters</span></span>
<span data-ttu-id="05ad3-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05ad3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ad3-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05ad3-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ad3-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05ad3-142">INPUTS</span></span>

### <span data-ttu-id="05ad3-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="05ad3-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05ad3-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="05ad3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="05ad3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="05ad3-145">System.String</span></span>

## <span data-ttu-id="05ad3-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05ad3-146">OUTPUTS</span></span>

### <span data-ttu-id="05ad3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05ad3-147">System.Boolean</span></span>

## <span data-ttu-id="05ad3-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="05ad3-148">NOTES</span></span>

## <span data-ttu-id="05ad3-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05ad3-149">RELATED LINKS</span></span>

[<span data-ttu-id="05ad3-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="05ad3-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="05ad3-151">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="05ad3-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="05ad3-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="05ad3-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
