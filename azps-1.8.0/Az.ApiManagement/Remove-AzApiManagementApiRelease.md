---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 0ff4f0cbf8cd2825c05ef30fa4bcb16a10e04a81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901689"
---
# <span data-ttu-id="285a9-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="285a9-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="285a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="285a9-102">SYNOPSIS</span></span>
<span data-ttu-id="285a9-103">Удаляет определенный выпуск API</span><span class="sxs-lookup"><span data-stu-id="285a9-103">Removes a particular API Release</span></span>

## <span data-ttu-id="285a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="285a9-104">SYNTAX</span></span>

### <span data-ttu-id="285a9-105">ByApiReleaseId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="285a9-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="285a9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="285a9-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="285a9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="285a9-107">DESCRIPTION</span></span>

<span data-ttu-id="285a9-108">Командлет **Remove-AzAzureRmApiManagementApiRelease** удаляет существующий выпуском API.</span><span class="sxs-lookup"><span data-stu-id="285a9-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="285a9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="285a9-109">EXAMPLES</span></span>

### <span data-ttu-id="285a9-110">Пример 1: удаление выпусков API</span><span class="sxs-lookup"><span data-stu-id="285a9-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="285a9-111">Эта команда удаляет выпуски API с указанными ApiId и ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="285a9-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="285a9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="285a9-112">PARAMETERS</span></span>

### <span data-ttu-id="285a9-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="285a9-113">-ApiId</span></span>
<span data-ttu-id="285a9-114">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="285a9-114">Identifier of the API.</span></span>
<span data-ttu-id="285a9-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="285a9-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285a9-116">-Context</span><span class="sxs-lookup"><span data-stu-id="285a9-116">-Context</span></span>
<span data-ttu-id="285a9-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="285a9-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="285a9-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="285a9-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="285a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285a9-119">-DefaultProfile</span></span>
<span data-ttu-id="285a9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="285a9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="285a9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="285a9-121">-InputObject</span></span>
<span data-ttu-id="285a9-122">Экземпляр PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="285a9-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="285a9-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="285a9-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="285a9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="285a9-124">-PassThru</span></span>
<span data-ttu-id="285a9-125">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="285a9-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="285a9-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="285a9-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="285a9-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="285a9-127">-ReleaseId</span></span>
<span data-ttu-id="285a9-128">Идентификатор выпусков API.</span><span class="sxs-lookup"><span data-stu-id="285a9-128">Identifier of the API Release.</span></span>
<span data-ttu-id="285a9-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="285a9-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285a9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="285a9-130">-Confirm</span></span>
<span data-ttu-id="285a9-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="285a9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="285a9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="285a9-132">-WhatIf</span></span>
<span data-ttu-id="285a9-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="285a9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="285a9-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="285a9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="285a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285a9-135">CommonParameters</span></span>
<span data-ttu-id="285a9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="285a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285a9-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285a9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285a9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="285a9-138">INPUTS</span></span>

### <span data-ttu-id="285a9-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="285a9-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="285a9-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="285a9-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="285a9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="285a9-141">System.String</span></span>

## <span data-ttu-id="285a9-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="285a9-142">OUTPUTS</span></span>

### <span data-ttu-id="285a9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="285a9-143">System.Boolean</span></span>

## <span data-ttu-id="285a9-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="285a9-144">NOTES</span></span>

## <span data-ttu-id="285a9-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="285a9-145">RELATED LINKS</span></span>

[<span data-ttu-id="285a9-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="285a9-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="285a9-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="285a9-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="285a9-148">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="285a9-148">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)