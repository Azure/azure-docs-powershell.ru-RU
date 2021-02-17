---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220473"
---
# <span data-ttu-id="07fa8-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="07fa8-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="07fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="07fa8-103">Создает определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="07fa8-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="07fa8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07fa8-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07fa8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="07fa8-106">Для создания управляемого определения приложения создается **cmdlet New-AzManagedApplicationDefinition.**</span><span class="sxs-lookup"><span data-stu-id="07fa8-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="07fa8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07fa8-107">EXAMPLES</span></span>

### <span data-ttu-id="07fa8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07fa8-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="07fa8-109">Эта команда создает управляемое определение приложения.</span><span class="sxs-lookup"><span data-stu-id="07fa8-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="07fa8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07fa8-110">PARAMETERS</span></span>

### <span data-ttu-id="07fa8-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="07fa8-111">-ApiVersion</span></span>
<span data-ttu-id="07fa8-112">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07fa8-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="07fa8-113">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="07fa8-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fa8-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="07fa8-114">-Authorization</span></span>
<span data-ttu-id="07fa8-115">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="07fa8-115">The managed application definition authorization.</span></span>
<span data-ttu-id="07fa8-116">Пары раздельных разделов авторизации в \<principalId\> формате:\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="07fa8-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07fa8-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="07fa8-117">-CreateUiDefinition</span></span>
<span data-ttu-id="07fa8-118">Определение пользовательского интерфейса в определении управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="07fa8-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="07fa8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07fa8-119">-DefaultProfile</span></span>
<span data-ttu-id="07fa8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07fa8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07fa8-121">-Description</span><span class="sxs-lookup"><span data-stu-id="07fa8-121">-Description</span></span>
<span data-ttu-id="07fa8-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="07fa8-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="07fa8-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="07fa8-123">-DisplayName</span></span>
<span data-ttu-id="07fa8-124">Отображаемая имя управляемого определения приложения.</span><span class="sxs-lookup"><span data-stu-id="07fa8-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="07fa8-125">-Location</span><span class="sxs-lookup"><span data-stu-id="07fa8-125">-Location</span></span>
<span data-ttu-id="07fa8-126">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="07fa8-126">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fa8-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="07fa8-127">-LockLevel</span></span>
<span data-ttu-id="07fa8-128">Уровень блокировки для определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="07fa8-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07fa8-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="07fa8-129">-MainTemplate</span></span>
<span data-ttu-id="07fa8-130">Основной шаблон определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="07fa8-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="07fa8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="07fa8-131">-Name</span></span>
<span data-ttu-id="07fa8-132">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="07fa8-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="07fa8-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="07fa8-133">-PackageFileUri</span></span>
<span data-ttu-id="07fa8-134">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="07fa8-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="07fa8-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="07fa8-135">-Pre</span></span>
<span data-ttu-id="07fa8-136">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="07fa8-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="07fa8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07fa8-137">-ResourceGroupName</span></span>
<span data-ttu-id="07fa8-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07fa8-138">The resource group name.</span></span>

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

### <span data-ttu-id="07fa8-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="07fa8-139">-Tag</span></span>
<span data-ttu-id="07fa8-140">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="07fa8-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07fa8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07fa8-141">-Confirm</span></span>
<span data-ttu-id="07fa8-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="07fa8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07fa8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07fa8-143">-WhatIf</span></span>
<span data-ttu-id="07fa8-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07fa8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07fa8-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="07fa8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07fa8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07fa8-146">CommonParameters</span></span>
<span data-ttu-id="07fa8-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07fa8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07fa8-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07fa8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07fa8-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07fa8-149">INPUTS</span></span>

### <span data-ttu-id="07fa8-150">System.String</span><span class="sxs-lookup"><span data-stu-id="07fa8-150">System.String</span></span>

### <span data-ttu-id="07fa8-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="07fa8-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="07fa8-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="07fa8-152">System.String[]</span></span>

### <span data-ttu-id="07fa8-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="07fa8-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="07fa8-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07fa8-154">OUTPUTS</span></span>

### <span data-ttu-id="07fa8-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="07fa8-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="07fa8-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07fa8-156">NOTES</span></span>

## <span data-ttu-id="07fa8-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07fa8-157">RELATED LINKS</span></span>
