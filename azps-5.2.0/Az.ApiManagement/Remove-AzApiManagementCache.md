---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411972"
---
# <span data-ttu-id="268dd-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="268dd-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="268dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268dd-102">SYNOPSIS</span></span>
<span data-ttu-id="268dd-103">Удаляет сущность кэша.</span><span class="sxs-lookup"><span data-stu-id="268dd-103">Removes the cache entity.</span></span>

## <span data-ttu-id="268dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="268dd-104">SYNTAX</span></span>

### <span data-ttu-id="268dd-105">ContextParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="268dd-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="268dd-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="268dd-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="268dd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="268dd-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="268dd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="268dd-108">DESCRIPTION</span></span>
<span data-ttu-id="268dd-109">Cmdlet **Remove-AzApiManagementCache** удаляет сущность кэша.</span><span class="sxs-lookup"><span data-stu-id="268dd-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="268dd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="268dd-110">EXAMPLES</span></span>

### <span data-ttu-id="268dd-111">Пример 1. Удаление сущности Cache</span><span class="sxs-lookup"><span data-stu-id="268dd-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="268dd-112">Этот cmdlet удаляет кэш из `centralus` службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="268dd-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="268dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="268dd-113">PARAMETERS</span></span>

### <span data-ttu-id="268dd-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="268dd-114">-CacheId</span></span>
<span data-ttu-id="268dd-115">Идентификатор существующего кэшаId.</span><span class="sxs-lookup"><span data-stu-id="268dd-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="268dd-116">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="268dd-116">This parameter is required.</span></span>

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

### <span data-ttu-id="268dd-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="268dd-117">-Context</span></span>
<span data-ttu-id="268dd-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="268dd-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="268dd-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="268dd-119">This parameter is required.</span></span>

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

### <span data-ttu-id="268dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268dd-120">-DefaultProfile</span></span>
<span data-ttu-id="268dd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="268dd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="268dd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="268dd-122">-InputObject</span></span>
<span data-ttu-id="268dd-123">Экземпляр PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="268dd-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="268dd-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="268dd-124">This parameter is required.</span></span>

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

### <span data-ttu-id="268dd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="268dd-125">-PassThru</span></span>
<span data-ttu-id="268dd-126">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="268dd-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="268dd-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="268dd-127">This parameter is optional.</span></span>
<span data-ttu-id="268dd-128">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="268dd-128">Default value is false.</span></span>

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

### <span data-ttu-id="268dd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="268dd-129">-ResourceId</span></span>
<span data-ttu-id="268dd-130">Arm ResourceId кэша.</span><span class="sxs-lookup"><span data-stu-id="268dd-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="268dd-131">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="268dd-131">This parameter is required.</span></span>

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

### <span data-ttu-id="268dd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="268dd-132">-Confirm</span></span>
<span data-ttu-id="268dd-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="268dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="268dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="268dd-134">-WhatIf</span></span>
<span data-ttu-id="268dd-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="268dd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="268dd-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="268dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="268dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268dd-137">CommonParameters</span></span>
<span data-ttu-id="268dd-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268dd-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="268dd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268dd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="268dd-140">INPUTS</span></span>

### <span data-ttu-id="268dd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="268dd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="268dd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="268dd-142">System.String</span></span>

### <span data-ttu-id="268dd-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="268dd-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="268dd-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="268dd-144">OUTPUTS</span></span>

### <span data-ttu-id="268dd-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="268dd-145">System.Boolean</span></span>

## <span data-ttu-id="268dd-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="268dd-146">NOTES</span></span>

## <span data-ttu-id="268dd-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="268dd-147">RELATED LINKS</span></span>

[<span data-ttu-id="268dd-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="268dd-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="268dd-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="268dd-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="268dd-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="268dd-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
