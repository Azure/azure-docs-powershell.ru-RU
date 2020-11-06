---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558595"
---
# <span data-ttu-id="e2772-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e2772-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="e2772-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2772-102">SYNOPSIS</span></span>
<span data-ttu-id="e2772-103">Обновляет определенный выпуск API.</span><span class="sxs-lookup"><span data-stu-id="e2772-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2772-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2772-104">SYNTAX</span></span>

### <span data-ttu-id="e2772-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2772-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2772-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2772-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2772-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2772-107">DESCRIPTION</span></span>
<span data-ttu-id="e2772-108">Командлет **Update-AzureRmApiManagementApiRelease** изменяет выпускную функцию API для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="e2772-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="e2772-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2772-109">EXAMPLES</span></span>

### <span data-ttu-id="e2772-110">Пример 1: Обновление выпусков API для редакции API</span><span class="sxs-lookup"><span data-stu-id="e2772-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="e2772-111">Эта команда обновляет `echo-api-release` выпуски API API `echo-api` с новой заметкой.</span><span class="sxs-lookup"><span data-stu-id="e2772-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="e2772-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2772-112">PARAMETERS</span></span>

### <span data-ttu-id="e2772-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e2772-113">-ApiId</span></span>
<span data-ttu-id="e2772-114">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="e2772-114">Identifier of existing API.</span></span>
<span data-ttu-id="e2772-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e2772-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2772-116">-Context</span><span class="sxs-lookup"><span data-stu-id="e2772-116">-Context</span></span>
<span data-ttu-id="e2772-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e2772-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e2772-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e2772-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2772-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2772-119">-DefaultProfile</span></span>
<span data-ttu-id="e2772-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2772-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2772-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2772-121">-InputObject</span></span>
<span data-ttu-id="e2772-122">Экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="e2772-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2772-123">-Примечание</span><span class="sxs-lookup"><span data-stu-id="e2772-123">-Note</span></span>
<span data-ttu-id="e2772-124">Заметки о выпуске API.</span><span class="sxs-lookup"><span data-stu-id="e2772-124">Api Release Notes.</span></span>
<span data-ttu-id="e2772-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e2772-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="e2772-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2772-126">-PassThru</span></span>
<span data-ttu-id="e2772-127">Если указан экземпляр Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease, представляющий выпуск API набора.</span><span class="sxs-lookup"><span data-stu-id="e2772-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="e2772-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="e2772-128">-ReleaseId</span></span>
<span data-ttu-id="e2772-129">Идентификатор для API редакции ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="e2772-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="e2772-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e2772-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2772-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2772-131">-Confirm</span></span>
<span data-ttu-id="e2772-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2772-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2772-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2772-133">-WhatIf</span></span>
<span data-ttu-id="e2772-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2772-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2772-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2772-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2772-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2772-136">CommonParameters</span></span>
<span data-ttu-id="e2772-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2772-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2772-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2772-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2772-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2772-139">INPUTS</span></span>

### <span data-ttu-id="e2772-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e2772-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="e2772-141">Параметры: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2772-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="e2772-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e2772-142">System.String</span></span>

### <span data-ttu-id="e2772-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e2772-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="e2772-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2772-144">OUTPUTS</span></span>

### <span data-ttu-id="e2772-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e2772-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="e2772-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2772-146">NOTES</span></span>

## <span data-ttu-id="e2772-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2772-147">RELATED LINKS</span></span>

[<span data-ttu-id="e2772-148">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e2772-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="e2772-149">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e2772-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)
