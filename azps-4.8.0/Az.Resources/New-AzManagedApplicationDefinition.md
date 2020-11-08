---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077658"
---
# <span data-ttu-id="a2162-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="a2162-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="a2162-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2162-102">SYNOPSIS</span></span>
<span data-ttu-id="a2162-103">Создание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="a2162-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2162-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2162-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2162-105">DESCRIPTION</span></span>
<span data-ttu-id="a2162-106">Командлет **New-AzManagedApplicationDefinition** создает определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="a2162-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2162-107">EXAMPLES</span></span>

### <span data-ttu-id="a2162-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2162-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="a2162-109">Эта команда создает определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="a2162-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2162-110">PARAMETERS</span></span>

### <span data-ttu-id="a2162-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a2162-111">-ApiVersion</span></span>
<span data-ttu-id="a2162-112">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2162-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a2162-113">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="a2162-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a2162-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="a2162-114">-Authorization</span></span>
<span data-ttu-id="a2162-115">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-115">The managed application definition authorization.</span></span>
<span data-ttu-id="a2162-116">Пары авторизации, разделенные запятыми, в формате \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="a2162-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="a2162-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="a2162-117">-CreateUiDefinition</span></span>
<span data-ttu-id="a2162-118">Определение пользовательского интерфейса создания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="a2162-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="a2162-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2162-119">-DefaultProfile</span></span>
<span data-ttu-id="a2162-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2162-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2162-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="a2162-121">-Description</span></span>
<span data-ttu-id="a2162-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="a2162-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a2162-123">-DisplayName</span></span>
<span data-ttu-id="a2162-124">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="a2162-125">-Location</span><span class="sxs-lookup"><span data-stu-id="a2162-125">-Location</span></span>
<span data-ttu-id="a2162-126">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a2162-126">The resource location.</span></span>

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

### <span data-ttu-id="a2162-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="a2162-127">-LockLevel</span></span>
<span data-ttu-id="a2162-128">Уровень блокировки для определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="a2162-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="a2162-129">-MainTemplate</span></span>
<span data-ttu-id="a2162-130">Основной шаблон определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="a2162-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="a2162-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2162-131">-Name</span></span>
<span data-ttu-id="a2162-132">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="a2162-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="a2162-133">-PackageFileUri</span></span>
<span data-ttu-id="a2162-134">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="a2162-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="a2162-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="a2162-135">-Pre</span></span>
<span data-ttu-id="a2162-136">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="a2162-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a2162-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2162-137">-ResourceGroupName</span></span>
<span data-ttu-id="a2162-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2162-138">The resource group name.</span></span>

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

### <span data-ttu-id="a2162-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="a2162-139">-Tag</span></span>
<span data-ttu-id="a2162-140">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2162-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a2162-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2162-141">-Confirm</span></span>
<span data-ttu-id="a2162-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2162-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2162-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2162-143">-WhatIf</span></span>
<span data-ttu-id="a2162-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2162-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2162-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2162-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2162-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2162-146">CommonParameters</span></span>
<span data-ttu-id="a2162-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2162-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2162-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2162-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2162-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2162-149">INPUTS</span></span>

### <span data-ttu-id="a2162-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a2162-150">System.String</span></span>

### <span data-ttu-id="a2162-151">Microsoft. Azure. Commands. ResourceManager. командлеты Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="a2162-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="a2162-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="a2162-152">System.String[]</span></span>

### <span data-ttu-id="a2162-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2162-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a2162-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2162-154">OUTPUTS</span></span>

### <span data-ttu-id="a2162-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a2162-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a2162-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2162-156">NOTES</span></span>

## <span data-ttu-id="a2162-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2162-157">RELATED LINKS</span></span>
