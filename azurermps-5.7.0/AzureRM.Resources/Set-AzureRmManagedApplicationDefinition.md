---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 8914b6d48b14ea372f29a6b7b0f5c9a1c32a6fd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557184"
---
# <span data-ttu-id="387dd-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="387dd-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="387dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="387dd-102">SYNOPSIS</span></span>
<span data-ttu-id="387dd-103">Обновляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="387dd-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="387dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="387dd-104">SYNTAX</span></span>

### <span data-ttu-id="387dd-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="387dd-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="387dd-106">SetById</span><span class="sxs-lookup"><span data-stu-id="387dd-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="387dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="387dd-107">DESCRIPTION</span></span>
<span data-ttu-id="387dd-108">Командлет **Set-AzureRmManagedApplicationDefinition** обновляет определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="387dd-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="387dd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="387dd-109">EXAMPLES</span></span>

### <span data-ttu-id="387dd-110">Пример 1: Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="387dd-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="387dd-111">Эта команда обновляет описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="387dd-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="387dd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="387dd-112">PARAMETERS</span></span>

### <span data-ttu-id="387dd-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="387dd-113">-ApiVersion</span></span>
<span data-ttu-id="387dd-114">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="387dd-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="387dd-115">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="387dd-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="387dd-116">-Authorization</span><span class="sxs-lookup"><span data-stu-id="387dd-116">-Authorization</span></span>
<span data-ttu-id="387dd-117">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="387dd-117">The managed application definition authorization.</span></span>
<span data-ttu-id="387dd-118">Пары авторизации, разделенные запятыми, в формате \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="387dd-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="387dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387dd-119">-DefaultProfile</span></span>
<span data-ttu-id="387dd-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="387dd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="387dd-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="387dd-121">-Description</span></span>
<span data-ttu-id="387dd-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="387dd-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="387dd-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="387dd-123">-DisplayName</span></span>
<span data-ttu-id="387dd-124">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="387dd-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="387dd-125">-ID</span><span class="sxs-lookup"><span data-stu-id="387dd-125">-Id</span></span>
<span data-ttu-id="387dd-126">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="387dd-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="387dd-127">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387dd-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="387dd-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="387dd-128">-Name</span></span>
<span data-ttu-id="387dd-129">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="387dd-129">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="387dd-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="387dd-130">-PackageFileUri</span></span>
<span data-ttu-id="387dd-131">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="387dd-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="387dd-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="387dd-132">-Pre</span></span>
<span data-ttu-id="387dd-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="387dd-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="387dd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387dd-134">-ResourceGroupName</span></span>
<span data-ttu-id="387dd-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="387dd-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="387dd-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="387dd-136">-Tag</span></span>
<span data-ttu-id="387dd-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="387dd-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="387dd-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="387dd-138">-Confirm</span></span>
<span data-ttu-id="387dd-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="387dd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="387dd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="387dd-140">-WhatIf</span></span>
<span data-ttu-id="387dd-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="387dd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="387dd-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="387dd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="387dd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387dd-143">CommonParameters</span></span>
<span data-ttu-id="387dd-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="387dd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387dd-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387dd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387dd-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="387dd-146">INPUTS</span></span>

### <span data-ttu-id="387dd-147">System. String</span><span class="sxs-lookup"><span data-stu-id="387dd-147">System.String</span></span>
<span data-ttu-id="387dd-148">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="387dd-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="387dd-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="387dd-149">OUTPUTS</span></span>

### <span data-ttu-id="387dd-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="387dd-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="387dd-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="387dd-151">NOTES</span></span>

## <span data-ttu-id="387dd-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="387dd-152">RELATED LINKS</span></span>
