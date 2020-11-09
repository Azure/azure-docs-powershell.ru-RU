---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315725"
---
# <span data-ttu-id="acc46-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="acc46-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="acc46-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="acc46-102">SYNOPSIS</span></span>
<span data-ttu-id="acc46-103">Создание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="acc46-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="acc46-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acc46-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acc46-105">DESCRIPTION</span></span>
<span data-ttu-id="acc46-106">Командлет **New-AzManagedApplicationDefinition** создает определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="acc46-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="acc46-107">EXAMPLES</span></span>

### <span data-ttu-id="acc46-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acc46-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="acc46-109">Эта команда создает определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="acc46-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="acc46-110">PARAMETERS</span></span>

### <span data-ttu-id="acc46-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="acc46-111">-ApiVersion</span></span>
<span data-ttu-id="acc46-112">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acc46-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="acc46-113">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="acc46-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="acc46-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="acc46-114">-Authorization</span></span>
<span data-ttu-id="acc46-115">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-115">The managed application definition authorization.</span></span>
<span data-ttu-id="acc46-116">Пары авторизации, разделенные запятыми, в формате \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="acc46-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="acc46-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="acc46-117">-CreateUiDefinition</span></span>
<span data-ttu-id="acc46-118">Определение пользовательского интерфейса создания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="acc46-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="acc46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc46-119">-DefaultProfile</span></span>
<span data-ttu-id="acc46-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acc46-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc46-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="acc46-121">-Description</span></span>
<span data-ttu-id="acc46-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="acc46-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="acc46-123">-DisplayName</span></span>
<span data-ttu-id="acc46-124">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="acc46-125">-Location</span><span class="sxs-lookup"><span data-stu-id="acc46-125">-Location</span></span>
<span data-ttu-id="acc46-126">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="acc46-126">The resource location.</span></span>

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

### <span data-ttu-id="acc46-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="acc46-127">-LockLevel</span></span>
<span data-ttu-id="acc46-128">Уровень блокировки для определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="acc46-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="acc46-129">-MainTemplate</span></span>
<span data-ttu-id="acc46-130">Основной шаблон определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="acc46-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="acc46-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="acc46-131">-Name</span></span>
<span data-ttu-id="acc46-132">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="acc46-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="acc46-133">-PackageFileUri</span></span>
<span data-ttu-id="acc46-134">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="acc46-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="acc46-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="acc46-135">-Pre</span></span>
<span data-ttu-id="acc46-136">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="acc46-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="acc46-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc46-137">-ResourceGroupName</span></span>
<span data-ttu-id="acc46-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acc46-138">The resource group name.</span></span>

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

### <span data-ttu-id="acc46-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="acc46-139">-Tag</span></span>
<span data-ttu-id="acc46-140">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acc46-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="acc46-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acc46-141">-Confirm</span></span>
<span data-ttu-id="acc46-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="acc46-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc46-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc46-143">-WhatIf</span></span>
<span data-ttu-id="acc46-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="acc46-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acc46-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="acc46-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc46-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc46-146">CommonParameters</span></span>
<span data-ttu-id="acc46-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="acc46-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc46-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acc46-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc46-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="acc46-149">INPUTS</span></span>

### <span data-ttu-id="acc46-150">System. String</span><span class="sxs-lookup"><span data-stu-id="acc46-150">System.String</span></span>

### <span data-ttu-id="acc46-151">Microsoft. Azure. Commands. ResourceManager. командлеты Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="acc46-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="acc46-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="acc46-152">System.String[]</span></span>

### <span data-ttu-id="acc46-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="acc46-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="acc46-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="acc46-154">OUTPUTS</span></span>

### <span data-ttu-id="acc46-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="acc46-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="acc46-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="acc46-156">NOTES</span></span>

## <span data-ttu-id="acc46-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acc46-157">RELATED LINKS</span></span>
