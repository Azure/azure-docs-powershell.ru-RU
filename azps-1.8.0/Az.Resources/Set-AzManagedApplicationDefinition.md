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
ms.locfileid: "93729317"
---
# <span data-ttu-id="8f31e-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="8f31e-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="8f31e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f31e-102">SYNOPSIS</span></span>
<span data-ttu-id="8f31e-103">Обновляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="8f31e-103">Updates managed application definition</span></span>

## <span data-ttu-id="8f31e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f31e-104">SYNTAX</span></span>

### <span data-ttu-id="8f31e-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f31e-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f31e-106">SetById</span><span class="sxs-lookup"><span data-stu-id="8f31e-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f31e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f31e-107">DESCRIPTION</span></span>
<span data-ttu-id="8f31e-108">Командлет **Set-AzManagedApplicationDefinition** обновляет определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="8f31e-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="8f31e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f31e-109">EXAMPLES</span></span>

### <span data-ttu-id="8f31e-110">Пример 1: Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="8f31e-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="8f31e-111">Эта команда обновляет описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8f31e-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="8f31e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f31e-112">PARAMETERS</span></span>

### <span data-ttu-id="8f31e-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f31e-113">-ApiVersion</span></span>
<span data-ttu-id="8f31e-114">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f31e-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f31e-115">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="8f31e-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8f31e-116">-Authorization</span><span class="sxs-lookup"><span data-stu-id="8f31e-116">-Authorization</span></span>
<span data-ttu-id="8f31e-117">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8f31e-117">The managed application definition authorization.</span></span>
<span data-ttu-id="8f31e-118">Пары авторизации, разделенные запятыми, в формате \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="8f31e-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="8f31e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f31e-119">-DefaultProfile</span></span>
<span data-ttu-id="8f31e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f31e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f31e-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="8f31e-121">-Description</span></span>
<span data-ttu-id="8f31e-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8f31e-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="8f31e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f31e-123">-DisplayName</span></span>
<span data-ttu-id="8f31e-124">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8f31e-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="8f31e-125">-ID</span><span class="sxs-lookup"><span data-stu-id="8f31e-125">-Id</span></span>
<span data-ttu-id="8f31e-126">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="8f31e-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="8f31e-127">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f31e-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="8f31e-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f31e-128">-Name</span></span>
<span data-ttu-id="8f31e-129">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8f31e-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="8f31e-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="8f31e-130">-PackageFileUri</span></span>
<span data-ttu-id="8f31e-131">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="8f31e-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="8f31e-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="8f31e-132">-Pre</span></span>
<span data-ttu-id="8f31e-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="8f31e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8f31e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f31e-134">-ResourceGroupName</span></span>
<span data-ttu-id="8f31e-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f31e-135">The resource group name.</span></span>

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

### <span data-ttu-id="8f31e-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="8f31e-136">-Tag</span></span>
<span data-ttu-id="8f31e-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f31e-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="8f31e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f31e-138">-Confirm</span></span>
<span data-ttu-id="8f31e-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f31e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f31e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f31e-140">-WhatIf</span></span>
<span data-ttu-id="8f31e-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f31e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f31e-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f31e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f31e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f31e-143">CommonParameters</span></span>
<span data-ttu-id="8f31e-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f31e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f31e-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f31e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f31e-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f31e-146">INPUTS</span></span>

### <span data-ttu-id="8f31e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8f31e-147">System.String</span></span>

### <span data-ttu-id="8f31e-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="8f31e-148">System.String[]</span></span>

### <span data-ttu-id="8f31e-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8f31e-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8f31e-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f31e-150">OUTPUTS</span></span>

### <span data-ttu-id="8f31e-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8f31e-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8f31e-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f31e-152">NOTES</span></span>

## <span data-ttu-id="8f31e-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f31e-153">RELATED LINKS</span></span>
