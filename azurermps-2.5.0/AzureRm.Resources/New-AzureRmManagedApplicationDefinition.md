---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: 3451a922af2b2af469b7edba1539f52cabb64eb2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914745"
---
# <span data-ttu-id="b7e77-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="b7e77-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="b7e77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7e77-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e77-103">Создание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7e77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7e77-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7e77-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7e77-105">DESCRIPTION</span></span>
<span data-ttu-id="b7e77-106">Командлет **New-AzureRmManagedApplicationDefinition** создает определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="b7e77-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7e77-107">EXAMPLES</span></span>

### <span data-ttu-id="b7e77-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7e77-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="b7e77-109">Эта команда создает определение управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="b7e77-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7e77-110">PARAMETERS</span></span>

### <span data-ttu-id="b7e77-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b7e77-111">-ApiVersion</span></span>
<span data-ttu-id="b7e77-112">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7e77-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b7e77-113">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="b7e77-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="b7e77-114">-Authorization</span></span>
<span data-ttu-id="b7e77-115">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-115">The managed application definition authorization.</span></span>
<span data-ttu-id="b7e77-116">Пары авторизации, разделенные запятыми, в формате \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="b7e77-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="b7e77-117">-CreateUiDefinition</span></span>
<span data-ttu-id="b7e77-118">Определение пользовательского интерфейса создания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="b7e77-118">The managed application definition create ui definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e77-119">-DefaultProfile</span></span>
<span data-ttu-id="b7e77-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e77-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="b7e77-121">-Description</span></span>
<span data-ttu-id="b7e77-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b7e77-123">-DisplayName</span></span>
<span data-ttu-id="b7e77-124">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-125">-Location</span><span class="sxs-lookup"><span data-stu-id="b7e77-125">-Location</span></span>
<span data-ttu-id="b7e77-126">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7e77-126">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="b7e77-127">-LockLevel</span></span>
<span data-ttu-id="b7e77-128">Уровень блокировки для определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="b7e77-129">-MainTemplate</span></span>
<span data-ttu-id="b7e77-130">Основной шаблон определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="b7e77-130">The managed application definition main template</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7e77-131">-Name</span></span>
<span data-ttu-id="b7e77-132">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-132">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="b7e77-133">-PackageFileUri</span></span>
<span data-ttu-id="b7e77-134">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b7e77-134">The managed application definition package file uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="b7e77-135">-Pre</span></span>
<span data-ttu-id="b7e77-136">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="b7e77-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e77-137">-ResourceGroupName</span></span>
<span data-ttu-id="b7e77-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7e77-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="b7e77-139">-Tag</span></span>
<span data-ttu-id="b7e77-140">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7e77-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7e77-141">-Confirm</span></span>
<span data-ttu-id="b7e77-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7e77-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e77-143">-WhatIf</span></span>
<span data-ttu-id="b7e77-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7e77-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7e77-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7e77-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e77-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e77-146">CommonParameters</span></span>
<span data-ttu-id="b7e77-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7e77-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e77-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e77-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e77-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7e77-149">INPUTS</span></span>

### <span data-ttu-id="b7e77-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b7e77-150">System.String</span></span>
<span data-ttu-id="b7e77-151">Microsoft. Azure. Commands. ResourceManager. командлеты. Entities. Application. ApplicationLockLevel System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7e77-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7e77-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7e77-152">OUTPUTS</span></span>

### <span data-ttu-id="b7e77-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b7e77-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b7e77-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7e77-154">NOTES</span></span>

## <span data-ttu-id="b7e77-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7e77-155">RELATED LINKS</span></span>
