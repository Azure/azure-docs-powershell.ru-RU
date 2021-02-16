---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216433"
---
# <span data-ttu-id="0eb20-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eb20-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="0eb20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb20-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb20-103">Публикует изменения, вносяые в базу данных конфигурации из ветви Git.</span><span class="sxs-lookup"><span data-stu-id="0eb20-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="0eb20-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0eb20-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0eb20-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0eb20-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb20-106">**Cmdlet Publish-AzApiManagementTenantGitConfiguration** публикует изменения из Ветвь Git в базу данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0eb20-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="0eb20-107">Кроме того, можно проверить изменения в ветвях Git, не публикуя их.</span><span class="sxs-lookup"><span data-stu-id="0eb20-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="0eb20-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0eb20-108">EXAMPLES</span></span>

### <span data-ttu-id="0eb20-109">Пример 1. Развертывание изменений GIT</span><span class="sxs-lookup"><span data-stu-id="0eb20-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="0eb20-110">Эта команда публикует изменения из указанной ветви в базе данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0eb20-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="0eb20-111">Пример 2. Проверка изменений GIT</span><span class="sxs-lookup"><span data-stu-id="0eb20-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="0eb20-112">Эта команда проверяет изменения в ветви Git на базе данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0eb20-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="0eb20-113">Изменения не публикуются.</span><span class="sxs-lookup"><span data-stu-id="0eb20-113">It does not publish changes.</span></span>

## <span data-ttu-id="0eb20-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eb20-114">PARAMETERS</span></span>

### <span data-ttu-id="0eb20-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="0eb20-115">-Branch</span></span>
<span data-ttu-id="0eb20-116">Имя ветви Git, из которой этот cmdlet развертывает конфигурацию в базе данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0eb20-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="0eb20-117">-Контекст</span><span class="sxs-lookup"><span data-stu-id="0eb20-117">-Context</span></span>
<span data-ttu-id="0eb20-118">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="0eb20-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb20-119">-DefaultProfile</span></span>
<span data-ttu-id="0eb20-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb20-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb20-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0eb20-121">-Force</span></span>
<span data-ttu-id="0eb20-122">Указывает на то, что этот cmdlet удаляет подписки на продукты, удаленные в этом обновлении.</span><span class="sxs-lookup"><span data-stu-id="0eb20-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="0eb20-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eb20-123">-PassThru</span></span>
<span data-ttu-id="0eb20-124">Указывает на то, что этот cmdlet возвращает объект **PsApiManagementOperationResult.**</span><span class="sxs-lookup"><span data-stu-id="0eb20-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="0eb20-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="0eb20-125">-ValidateOnly</span></span>
<span data-ttu-id="0eb20-126">Указывает на то, что этот cmdlet проверяет изменения в указанной ветви Git.</span><span class="sxs-lookup"><span data-stu-id="0eb20-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="0eb20-127">Она не публикуется в базе данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0eb20-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="0eb20-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0eb20-128">-Confirm</span></span>
<span data-ttu-id="0eb20-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb20-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb20-130">-WhatIf</span></span>
<span data-ttu-id="0eb20-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb20-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb20-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0eb20-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb20-133">CommonParameters</span></span>
<span data-ttu-id="0eb20-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb20-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0eb20-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb20-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0eb20-136">INPUTS</span></span>

### <span data-ttu-id="0eb20-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0eb20-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0eb20-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0eb20-138">System.String</span></span>

### <span data-ttu-id="0eb20-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0eb20-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0eb20-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0eb20-140">OUTPUTS</span></span>

### <span data-ttu-id="0eb20-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="0eb20-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="0eb20-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0eb20-142">NOTES</span></span>

## <span data-ttu-id="0eb20-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0eb20-143">RELATED LINKS</span></span>

[<span data-ttu-id="0eb20-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eb20-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


