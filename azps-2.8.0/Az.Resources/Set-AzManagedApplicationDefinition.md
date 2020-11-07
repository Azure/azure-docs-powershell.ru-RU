---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: d1da0ce7f8a88a12b0714960a60d5b2aa523a0a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905517"
---
# <span data-ttu-id="0b8c9-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="0b8c9-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="0b8c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8c9-103">Обновляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="0b8c9-103">Updates managed application definition</span></span>

## <span data-ttu-id="0b8c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b8c9-104">SYNTAX</span></span>

### <span data-ttu-id="0b8c9-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b8c9-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b8c9-106">SetById</span><span class="sxs-lookup"><span data-stu-id="0b8c9-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b8c9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b8c9-107">DESCRIPTION</span></span>
<span data-ttu-id="0b8c9-108">Командлет **Set-AzManagedApplicationDefinition** обновляет определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="0b8c9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b8c9-109">EXAMPLES</span></span>

### <span data-ttu-id="0b8c9-110">Пример 1: Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="0b8c9-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="0b8c9-111">Эта команда обновляет описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="0b8c9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b8c9-112">PARAMETERS</span></span>

### <span data-ttu-id="0b8c9-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0b8c9-113">-ApiVersion</span></span>
<span data-ttu-id="0b8c9-114">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0b8c9-115">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0b8c9-116">-Authorization</span><span class="sxs-lookup"><span data-stu-id="0b8c9-116">-Authorization</span></span>
<span data-ttu-id="0b8c9-117">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-117">The managed application definition authorization.</span></span>
<span data-ttu-id="0b8c9-118">Пары авторизации, разделенные запятыми, в формате \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="0b8c9-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8c9-119">-DefaultProfile</span></span>
<span data-ttu-id="0b8c9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b8c9-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="0b8c9-121">-Description</span></span>
<span data-ttu-id="0b8c9-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="0b8c9-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0b8c9-123">-DisplayName</span></span>
<span data-ttu-id="0b8c9-124">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="0b8c9-125">-ID</span><span class="sxs-lookup"><span data-stu-id="0b8c9-125">-Id</span></span>
<span data-ttu-id="0b8c9-126">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="0b8c9-127">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b8c9-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8c9-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b8c9-128">-Name</span></span>
<span data-ttu-id="0b8c9-129">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8c9-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="0b8c9-130">-PackageFileUri</span></span>
<span data-ttu-id="0b8c9-131">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="0b8c9-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="0b8c9-132">-Pre</span></span>
<span data-ttu-id="0b8c9-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0b8c9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b8c9-134">-ResourceGroupName</span></span>
<span data-ttu-id="0b8c9-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8c9-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="0b8c9-136">-Tag</span></span>
<span data-ttu-id="0b8c9-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0b8c9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b8c9-138">-Confirm</span></span>
<span data-ttu-id="0b8c9-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b8c9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b8c9-140">-WhatIf</span></span>
<span data-ttu-id="0b8c9-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b8c9-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b8c9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8c9-143">CommonParameters</span></span>
<span data-ttu-id="0b8c9-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b8c9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8c9-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b8c9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8c9-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b8c9-146">INPUTS</span></span>

### <span data-ttu-id="0b8c9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0b8c9-147">System.String</span></span>

### <span data-ttu-id="0b8c9-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="0b8c9-148">System.String[]</span></span>

### <span data-ttu-id="0b8c9-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b8c9-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b8c9-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b8c9-150">OUTPUTS</span></span>

### <span data-ttu-id="0b8c9-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0b8c9-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0b8c9-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b8c9-152">NOTES</span></span>

## <span data-ttu-id="0b8c9-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b8c9-153">RELATED LINKS</span></span>
