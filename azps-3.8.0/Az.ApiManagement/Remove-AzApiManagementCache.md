---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: 26704dd0ff44bf8a9e96dde15ebd52b57fa17ae2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414566"
---
# <span data-ttu-id="22115-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="22115-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="22115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22115-102">SYNOPSIS</span></span>
<span data-ttu-id="22115-103">Удаляет сущность кэша.</span><span class="sxs-lookup"><span data-stu-id="22115-103">Removes the cache entity.</span></span>

## <span data-ttu-id="22115-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22115-104">SYNTAX</span></span>

### <span data-ttu-id="22115-105">ContextParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22115-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22115-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22115-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22115-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22115-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22115-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22115-108">DESCRIPTION</span></span>
<span data-ttu-id="22115-109">С его выполнения **удаляется** объект кэша.</span><span class="sxs-lookup"><span data-stu-id="22115-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="22115-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22115-110">EXAMPLES</span></span>

### <span data-ttu-id="22115-111">Пример 1. Удаление сущности Cache</span><span class="sxs-lookup"><span data-stu-id="22115-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="22115-112">Этот cmdlet удаляет кэш из `centralus` службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="22115-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="22115-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22115-113">PARAMETERS</span></span>

### <span data-ttu-id="22115-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="22115-114">-CacheId</span></span>
<span data-ttu-id="22115-115">Идентификатор существующего кэшаId.</span><span class="sxs-lookup"><span data-stu-id="22115-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="22115-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="22115-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22115-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="22115-117">-Context</span></span>
<span data-ttu-id="22115-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="22115-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="22115-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="22115-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22115-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22115-120">-DefaultProfile</span></span>
<span data-ttu-id="22115-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22115-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22115-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22115-122">-InputObject</span></span>
<span data-ttu-id="22115-123">Экземпляр PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="22115-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="22115-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="22115-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22115-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22115-125">-PassThru</span></span>
<span data-ttu-id="22115-126">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="22115-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="22115-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="22115-127">This parameter is optional.</span></span>
<span data-ttu-id="22115-128">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="22115-128">Default value is false.</span></span>

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

### <span data-ttu-id="22115-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22115-129">-ResourceId</span></span>
<span data-ttu-id="22115-130">Arm ResourceId кэша.</span><span class="sxs-lookup"><span data-stu-id="22115-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="22115-131">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="22115-131">This parameter is required.</span></span>

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

### <span data-ttu-id="22115-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22115-132">-Confirm</span></span>
<span data-ttu-id="22115-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="22115-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22115-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22115-134">-WhatIf</span></span>
<span data-ttu-id="22115-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22115-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22115-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22115-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22115-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22115-137">CommonParameters</span></span>
<span data-ttu-id="22115-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22115-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22115-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22115-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22115-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22115-140">INPUTS</span></span>

### <span data-ttu-id="22115-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="22115-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="22115-142">System.String</span><span class="sxs-lookup"><span data-stu-id="22115-142">System.String</span></span>

### <span data-ttu-id="22115-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22115-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22115-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22115-144">OUTPUTS</span></span>

### <span data-ttu-id="22115-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22115-145">System.Boolean</span></span>

## <span data-ttu-id="22115-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22115-146">NOTES</span></span>

## <span data-ttu-id="22115-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22115-147">RELATED LINKS</span></span>

[<span data-ttu-id="22115-148">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="22115-148">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="22115-149">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="22115-149">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="22115-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="22115-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
