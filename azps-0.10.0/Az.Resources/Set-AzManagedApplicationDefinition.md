---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: 3d6a5488e7e101c904e90d056c8b2ffc03e786fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910830"
---
# <span data-ttu-id="9050f-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="9050f-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="9050f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9050f-102">SYNOPSIS</span></span>
<span data-ttu-id="9050f-103">Обновляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="9050f-103">Updates managed application definition</span></span>

## <span data-ttu-id="9050f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9050f-104">SYNTAX</span></span>

### <span data-ttu-id="9050f-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9050f-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9050f-106">SetById</span><span class="sxs-lookup"><span data-stu-id="9050f-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9050f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9050f-107">DESCRIPTION</span></span>
<span data-ttu-id="9050f-108">Командлет **Set-AzManagedApplicationDefinition** обновляет определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="9050f-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="9050f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9050f-109">EXAMPLES</span></span>

### <span data-ttu-id="9050f-110">Пример 1: Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="9050f-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="9050f-111">Эта команда обновляет описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="9050f-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="9050f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9050f-112">PARAMETERS</span></span>

### <span data-ttu-id="9050f-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9050f-113">-ApiVersion</span></span>
<span data-ttu-id="9050f-114">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9050f-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9050f-115">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="9050f-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9050f-116">-Authorization</span><span class="sxs-lookup"><span data-stu-id="9050f-116">-Authorization</span></span>
<span data-ttu-id="9050f-117">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="9050f-117">The managed application definition authorization.</span></span>
<span data-ttu-id="9050f-118">Пары авторизации, разделенные запятыми, в формате \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="9050f-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="9050f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9050f-119">-DefaultProfile</span></span>
<span data-ttu-id="9050f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9050f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9050f-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="9050f-121">-Description</span></span>
<span data-ttu-id="9050f-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="9050f-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="9050f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9050f-123">-DisplayName</span></span>
<span data-ttu-id="9050f-124">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="9050f-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="9050f-125">-ID</span><span class="sxs-lookup"><span data-stu-id="9050f-125">-Id</span></span>
<span data-ttu-id="9050f-126">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="9050f-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="9050f-127">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9050f-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="9050f-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9050f-128">-Name</span></span>
<span data-ttu-id="9050f-129">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="9050f-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="9050f-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="9050f-130">-PackageFileUri</span></span>
<span data-ttu-id="9050f-131">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="9050f-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="9050f-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="9050f-132">-Pre</span></span>
<span data-ttu-id="9050f-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="9050f-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9050f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9050f-134">-ResourceGroupName</span></span>
<span data-ttu-id="9050f-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9050f-135">The resource group name.</span></span>

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

### <span data-ttu-id="9050f-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="9050f-136">-Tag</span></span>
<span data-ttu-id="9050f-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9050f-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="9050f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9050f-138">-Confirm</span></span>
<span data-ttu-id="9050f-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9050f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9050f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9050f-140">-WhatIf</span></span>
<span data-ttu-id="9050f-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9050f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9050f-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9050f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9050f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9050f-143">CommonParameters</span></span>
<span data-ttu-id="9050f-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9050f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9050f-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9050f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9050f-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9050f-146">INPUTS</span></span>

### <span data-ttu-id="9050f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9050f-147">System.String</span></span>

### <span data-ttu-id="9050f-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="9050f-148">System.String[]</span></span>

### <span data-ttu-id="9050f-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9050f-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9050f-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9050f-150">OUTPUTS</span></span>

### <span data-ttu-id="9050f-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9050f-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9050f-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="9050f-152">NOTES</span></span>

## <span data-ttu-id="9050f-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9050f-153">RELATED LINKS</span></span>
