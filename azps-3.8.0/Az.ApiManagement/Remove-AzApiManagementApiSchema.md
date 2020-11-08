---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: fb144bfa228b07501c374f054970d1e3e0337ec1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075069"
---
# <span data-ttu-id="c9eb7-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c9eb7-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="c9eb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eb7-103">Удаляет схему API из API.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="c9eb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9eb7-104">SYNTAX</span></span>

### <span data-ttu-id="c9eb7-105">ByApiSchemaId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9eb7-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9eb7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c9eb7-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9eb7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9eb7-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9eb7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9eb7-108">DESCRIPTION</span></span>
<span data-ttu-id="c9eb7-109">Командлет **Remove-AzApiManagementSchema** из API.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="c9eb7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9eb7-110">EXAMPLES</span></span>

### <span data-ttu-id="c9eb7-111">Пример 1: удаление схемы API из API</span><span class="sxs-lookup"><span data-stu-id="c9eb7-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="c9eb7-112">Сценарий удаляет схему `2` из API, `echo-api` если она не указана.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="c9eb7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9eb7-113">PARAMETERS</span></span>

### <span data-ttu-id="c9eb7-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c9eb7-114">-ApiId</span></span>
<span data-ttu-id="c9eb7-115">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-115">Identifier of the API.</span></span>
<span data-ttu-id="c9eb7-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-116">This parameter is required.</span></span>

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

### <span data-ttu-id="c9eb7-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c9eb7-117">-Context</span></span>
<span data-ttu-id="c9eb7-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c9eb7-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c9eb7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eb7-120">-DefaultProfile</span></span>
<span data-ttu-id="c9eb7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9eb7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9eb7-122">-InputObject</span></span>
<span data-ttu-id="c9eb7-123">Экземпляр PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="c9eb7-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-124">This parameter is required.</span></span>

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

### <span data-ttu-id="c9eb7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9eb7-125">-PassThru</span></span>
<span data-ttu-id="c9eb7-126">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c9eb7-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="c9eb7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9eb7-128">-ResourceId</span></span>
<span data-ttu-id="c9eb7-129">ИД ResourceId для ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="c9eb7-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-130">This parameter is required.</span></span>

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

### <span data-ttu-id="c9eb7-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="c9eb7-131">-SchemaId</span></span>
<span data-ttu-id="c9eb7-132">Идентификатор схемы API.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="c9eb7-133">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-133">This parameter is required.</span></span>

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

### <span data-ttu-id="c9eb7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9eb7-134">-Confirm</span></span>
<span data-ttu-id="c9eb7-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9eb7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9eb7-136">-WhatIf</span></span>
<span data-ttu-id="c9eb7-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9eb7-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9eb7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eb7-139">CommonParameters</span></span>
<span data-ttu-id="c9eb7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9eb7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eb7-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9eb7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eb7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9eb7-142">INPUTS</span></span>

### <span data-ttu-id="c9eb7-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c9eb7-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c9eb7-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c9eb7-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="c9eb7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c9eb7-145">System.String</span></span>

## <span data-ttu-id="c9eb7-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9eb7-146">OUTPUTS</span></span>

### <span data-ttu-id="c9eb7-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9eb7-147">System.Boolean</span></span>

## <span data-ttu-id="c9eb7-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9eb7-148">NOTES</span></span>

## <span data-ttu-id="c9eb7-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9eb7-149">RELATED LINKS</span></span>

[<span data-ttu-id="c9eb7-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c9eb7-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="c9eb7-151">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c9eb7-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="c9eb7-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="c9eb7-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
