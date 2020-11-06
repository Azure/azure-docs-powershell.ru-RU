---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556959"
---
# <span data-ttu-id="fc597-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fc597-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="fc597-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc597-102">SYNOPSIS</span></span>
<span data-ttu-id="fc597-103">Удаляет определенный выпуск API</span><span class="sxs-lookup"><span data-stu-id="fc597-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc597-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc597-104">SYNTAX</span></span>

### <span data-ttu-id="fc597-105">ByApiReleaseId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc597-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc597-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc597-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc597-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc597-107">DESCRIPTION</span></span>

<span data-ttu-id="fc597-108">Командлет **Remove-AzureRmApiManagementApiRelease** удаляет существующий выпуском API.</span><span class="sxs-lookup"><span data-stu-id="fc597-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="fc597-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc597-109">EXAMPLES</span></span>

### <span data-ttu-id="fc597-110">Пример 1: удаление выпусков API</span><span class="sxs-lookup"><span data-stu-id="fc597-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="fc597-111">Эта команда удаляет выпуски API с указанными ApiId и ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="fc597-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="fc597-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc597-112">PARAMETERS</span></span>

### <span data-ttu-id="fc597-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fc597-113">-ApiId</span></span>
<span data-ttu-id="fc597-114">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="fc597-114">Identifier of the API.</span></span>
<span data-ttu-id="fc597-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fc597-115">This parameter is required.</span></span>

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

### <span data-ttu-id="fc597-116">-Context</span><span class="sxs-lookup"><span data-stu-id="fc597-116">-Context</span></span>
<span data-ttu-id="fc597-117">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fc597-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fc597-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fc597-118">This parameter is required.</span></span>

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

### <span data-ttu-id="fc597-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc597-119">-DefaultProfile</span></span>
<span data-ttu-id="fc597-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc597-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc597-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc597-121">-InputObject</span></span>
<span data-ttu-id="fc597-122">Экземпляр PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="fc597-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="fc597-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fc597-123">This parameter is required.</span></span>

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

### <span data-ttu-id="fc597-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc597-124">-PassThru</span></span>
<span data-ttu-id="fc597-125">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="fc597-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="fc597-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fc597-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc597-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="fc597-127">-ReleaseId</span></span>
<span data-ttu-id="fc597-128">Идентификатор выпусков API.</span><span class="sxs-lookup"><span data-stu-id="fc597-128">Identifier of the API Release.</span></span>
<span data-ttu-id="fc597-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fc597-129">This parameter is required.</span></span>

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

### <span data-ttu-id="fc597-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc597-130">-Confirm</span></span>
<span data-ttu-id="fc597-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc597-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc597-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc597-132">-WhatIf</span></span>
<span data-ttu-id="fc597-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc597-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc597-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc597-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc597-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc597-135">CommonParameters</span></span>
<span data-ttu-id="fc597-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc597-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc597-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc597-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc597-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc597-138">INPUTS</span></span>

### <span data-ttu-id="fc597-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fc597-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fc597-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fc597-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="fc597-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fc597-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="fc597-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fc597-142">System.String</span></span>

## <span data-ttu-id="fc597-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc597-143">OUTPUTS</span></span>

### <span data-ttu-id="fc597-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc597-144">System.Boolean</span></span>

## <span data-ttu-id="fc597-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc597-145">NOTES</span></span>

## <span data-ttu-id="fc597-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc597-146">RELATED LINKS</span></span>

[<span data-ttu-id="fc597-147">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fc597-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="fc597-148">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fc597-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="fc597-149">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="fc597-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
