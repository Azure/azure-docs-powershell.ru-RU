---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556955"
---
# <span data-ttu-id="30240-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="30240-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="30240-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30240-102">SYNOPSIS</span></span>
<span data-ttu-id="30240-103">Удалена определенная версия API</span><span class="sxs-lookup"><span data-stu-id="30240-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30240-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30240-104">SYNTAX</span></span>

### <span data-ttu-id="30240-105">ByApiId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30240-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30240-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="30240-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30240-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30240-107">DESCRIPTION</span></span>
<span data-ttu-id="30240-108">Командлет **Remove-AzureRmApiManagementApiRevision** Удаляет определенную редакцию API.</span><span class="sxs-lookup"><span data-stu-id="30240-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="30240-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30240-109">EXAMPLES</span></span>

### <span data-ttu-id="30240-110">Пример 1: удаление редакции API</span><span class="sxs-lookup"><span data-stu-id="30240-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="30240-111">Эта команда удаляет `2` редакцию API `echo-api` из службы управления API.</span><span class="sxs-lookup"><span data-stu-id="30240-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="30240-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30240-112">PARAMETERS</span></span>

### <span data-ttu-id="30240-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="30240-113">-ApiId</span></span>
<span data-ttu-id="30240-114">Идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="30240-114">Identifier of the API.</span></span>
<span data-ttu-id="30240-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="30240-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30240-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="30240-116">-ApiRevision</span></span>
<span data-ttu-id="30240-117">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="30240-117">Identifier of the API Revision.</span></span> <span data-ttu-id="30240-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="30240-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30240-119">-Context</span><span class="sxs-lookup"><span data-stu-id="30240-119">-Context</span></span>
<span data-ttu-id="30240-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="30240-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="30240-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="30240-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30240-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30240-122">-DefaultProfile</span></span>
<span data-ttu-id="30240-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30240-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30240-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30240-124">-InputObject</span></span>
<span data-ttu-id="30240-125">Экземпляр PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="30240-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="30240-126">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="30240-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30240-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30240-127">-PassThru</span></span>
<span data-ttu-id="30240-128">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="30240-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="30240-129">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="30240-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="30240-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30240-130">-Confirm</span></span>
<span data-ttu-id="30240-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30240-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30240-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30240-132">-WhatIf</span></span>
<span data-ttu-id="30240-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30240-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30240-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30240-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30240-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30240-135">CommonParameters</span></span>
<span data-ttu-id="30240-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30240-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30240-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30240-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30240-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30240-138">INPUTS</span></span>

### <span data-ttu-id="30240-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="30240-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="30240-140">System. String</span><span class="sxs-lookup"><span data-stu-id="30240-140">System.String</span></span>

### <span data-ttu-id="30240-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="30240-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="30240-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30240-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="30240-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30240-143">OUTPUTS</span></span>

### <span data-ttu-id="30240-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30240-144">System.Boolean</span></span>

## <span data-ttu-id="30240-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="30240-145">NOTES</span></span>

## <span data-ttu-id="30240-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30240-146">RELATED LINKS</span></span>

[<span data-ttu-id="30240-147">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="30240-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="30240-148">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="30240-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="30240-149">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="30240-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
