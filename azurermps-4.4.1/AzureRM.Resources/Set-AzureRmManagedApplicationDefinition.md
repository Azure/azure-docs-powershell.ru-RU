---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559536"
---
# <span data-ttu-id="b5471-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="b5471-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="b5471-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5471-102">SYNOPSIS</span></span>
<span data-ttu-id="b5471-103">Обновляет определение управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="b5471-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5471-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5471-104">SYNTAX</span></span>

### <span data-ttu-id="b5471-105">Заданный параметр имени определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b5471-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="b5471-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="b5471-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5471-107">Заданный параметр идентификатора определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b5471-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5471-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5471-108">DESCRIPTION</span></span>
<span data-ttu-id="b5471-109">Командлет **Set-AzureRmManagedApplicationDefinition** обновляет определения управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="b5471-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="b5471-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5471-110">EXAMPLES</span></span>

### <span data-ttu-id="b5471-111">Пример 1: Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="b5471-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="b5471-112">Эта команда обновляет описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b5471-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="b5471-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5471-113">PARAMETERS</span></span>

### <span data-ttu-id="b5471-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b5471-114">-ApiVersion</span></span>
<span data-ttu-id="b5471-115">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5471-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b5471-116">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="b5471-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b5471-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="b5471-117">-Authorization</span></span>
<span data-ttu-id="b5471-118">Авторизация определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b5471-118">The managed application definition authorization.</span></span>
<span data-ttu-id="b5471-119">Пары авторизации, разделенные запятыми, в формате \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="b5471-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="b5471-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5471-120">-DefaultProfile</span></span>
<span data-ttu-id="b5471-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5471-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5471-122">-Описание</span><span class="sxs-lookup"><span data-stu-id="b5471-122">-Description</span></span>
<span data-ttu-id="b5471-123">Описание определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b5471-123">The managed application definition description.</span></span>

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

### <span data-ttu-id="b5471-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b5471-124">-DisplayName</span></span>
<span data-ttu-id="b5471-125">Отображаемое имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b5471-125">The managed application definition display name.</span></span>

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

### <span data-ttu-id="b5471-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5471-126">-Name</span></span>
<span data-ttu-id="b5471-127">Имя определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b5471-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5471-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="b5471-128">-PackageFileUri</span></span>
<span data-ttu-id="b5471-129">URI файла пакета определения управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="b5471-129">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="b5471-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="b5471-130">-Pre</span></span>
<span data-ttu-id="b5471-131">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="b5471-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b5471-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5471-132">-ResourceGroupName</span></span>
<span data-ttu-id="b5471-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5471-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5471-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="b5471-134">-Tag</span></span>
<span data-ttu-id="b5471-135">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5471-135">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b5471-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5471-136">-Confirm</span></span>
<span data-ttu-id="b5471-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5471-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5471-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5471-138">-WhatIf</span></span>
<span data-ttu-id="b5471-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5471-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5471-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5471-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5471-141">-ID</span><span class="sxs-lookup"><span data-stu-id="b5471-141">-Id</span></span>
<span data-ttu-id="b5471-142">Полный идентификатор определения управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="b5471-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="b5471-143">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b5471-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5471-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5471-144">CommonParameters</span></span>
<span data-ttu-id="b5471-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5471-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5471-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5471-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5471-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5471-147">INPUTS</span></span>

### <span data-ttu-id="b5471-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b5471-148">System.String</span></span>
<span data-ttu-id="b5471-149">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b5471-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="b5471-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5471-150">OUTPUTS</span></span>

### <span data-ttu-id="b5471-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b5471-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b5471-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5471-152">NOTES</span></span>

## <span data-ttu-id="b5471-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5471-153">RELATED LINKS</span></span>

