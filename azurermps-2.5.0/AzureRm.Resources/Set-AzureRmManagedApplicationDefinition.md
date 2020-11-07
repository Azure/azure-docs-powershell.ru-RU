---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: ba2d158257f4be0e0daac8de5dd77e906e0abedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913550"
---
# <span data-ttu-id="320aa-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="320aa-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="320aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="320aa-102">SYNOPSIS</span></span>
<span data-ttu-id="320aa-103">Обновляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="320aa-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="320aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="320aa-104">SYNTAX</span></span>

### <span data-ttu-id="320aa-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="320aa-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="320aa-106">SetById</span><span class="sxs-lookup"><span data-stu-id="320aa-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320aa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="320aa-107">DESCRIPTION</span></span>
<span data-ttu-id="320aa-108">Командлет **Set-AzureRmManagedApplicationDefinition** обновляет определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="320aa-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="320aa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="320aa-109">EXAMPLES</span></span>

### <span data-ttu-id="320aa-110">Пример 1: Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="320aa-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="320aa-111">Эта команда обновляет описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="320aa-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="320aa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="320aa-112">PARAMETERS</span></span>

### <span data-ttu-id="320aa-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="320aa-113">-ApiVersion</span></span>
<span data-ttu-id="320aa-114">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="320aa-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="320aa-115">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="320aa-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="320aa-116">-Authorization</span><span class="sxs-lookup"><span data-stu-id="320aa-116">-Authorization</span></span>
<span data-ttu-id="320aa-117">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="320aa-117">The managed application definition authorization.</span></span>
<span data-ttu-id="320aa-118">Пары авторизации, разделенные запятыми, в формате \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="320aa-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="320aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320aa-119">-DefaultProfile</span></span>
<span data-ttu-id="320aa-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="320aa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="320aa-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="320aa-121">-Description</span></span>
<span data-ttu-id="320aa-122">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="320aa-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="320aa-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="320aa-123">-DisplayName</span></span>
<span data-ttu-id="320aa-124">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="320aa-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="320aa-125">-ID</span><span class="sxs-lookup"><span data-stu-id="320aa-125">-Id</span></span>
<span data-ttu-id="320aa-126">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="320aa-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="320aa-127">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320aa-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="320aa-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="320aa-128">-Name</span></span>
<span data-ttu-id="320aa-129">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="320aa-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="320aa-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="320aa-130">-PackageFileUri</span></span>
<span data-ttu-id="320aa-131">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="320aa-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="320aa-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="320aa-132">-Pre</span></span>
<span data-ttu-id="320aa-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="320aa-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="320aa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320aa-134">-ResourceGroupName</span></span>
<span data-ttu-id="320aa-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="320aa-135">The resource group name.</span></span>

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

### <span data-ttu-id="320aa-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="320aa-136">-Tag</span></span>
<span data-ttu-id="320aa-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="320aa-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="320aa-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="320aa-138">-Confirm</span></span>
<span data-ttu-id="320aa-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="320aa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320aa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320aa-140">-WhatIf</span></span>
<span data-ttu-id="320aa-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="320aa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320aa-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="320aa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320aa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320aa-143">CommonParameters</span></span>
<span data-ttu-id="320aa-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="320aa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320aa-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320aa-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320aa-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="320aa-146">INPUTS</span></span>

### <span data-ttu-id="320aa-147">System. String</span><span class="sxs-lookup"><span data-stu-id="320aa-147">System.String</span></span>
<span data-ttu-id="320aa-148">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="320aa-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="320aa-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="320aa-149">OUTPUTS</span></span>

### <span data-ttu-id="320aa-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="320aa-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="320aa-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="320aa-151">NOTES</span></span>

## <span data-ttu-id="320aa-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="320aa-152">RELATED LINKS</span></span>
