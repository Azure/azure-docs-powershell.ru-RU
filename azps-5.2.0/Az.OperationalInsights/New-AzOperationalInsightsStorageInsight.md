---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327182"
---
# <span data-ttu-id="317b6-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="317b6-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="317b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="317b6-102">SYNOPSIS</span></span>
<span data-ttu-id="317b6-103">Создание статистики хранилища в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="317b6-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="317b6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="317b6-104">SYNTAX</span></span>

### <span data-ttu-id="317b6-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="317b6-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="317b6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="317b6-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="317b6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="317b6-107">DESCRIPTION</span></span>
<span data-ttu-id="317b6-108">Для создания новой информации о хранилище в существующей рабочей области будет создаваться cmdlet **New-AzOperationalInsightStorageInsight.**</span><span class="sxs-lookup"><span data-stu-id="317b6-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="317b6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="317b6-109">EXAMPLES</span></span>

### <span data-ttu-id="317b6-110">Пример 1. Создание статистики хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="317b6-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="317b6-111">Первая команда использует Get-AzStorageAccount для получения учетной записи хранения ContosoStorage, а затем сохраняет ее $Storage переменной.</span><span class="sxs-lookup"><span data-stu-id="317b6-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="317b6-112">Вторая команда передает учетную запись хранения в $Storage командлету Get-AzStorageAccountKey, используя оператор конвейера для получения указанного ключа учетной записи хранения, а затем сохраняет его в переменной $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="317b6-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="317b6-113">В этом примере извлекется первый ключ.</span><span class="sxs-lookup"><span data-stu-id="317b6-113">This example retrieves the first key.</span></span> <span data-ttu-id="317b6-114">Чтобы получить другое значение, используйте значение[1] вместо value[0].</span><span class="sxs-lookup"><span data-stu-id="317b6-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="317b6-115">Конечная команда создает представление хранилища MyStorageInsight в рабочей области MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="317b6-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="317b6-116">Данные хранилища анализировали данные из таблицы WADWindowsEventLogsTable в указанном ресурсе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="317b6-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="317b6-117">Пример 2. Создание статистики хранилища с помощью объекта рабочей области</span><span class="sxs-lookup"><span data-stu-id="317b6-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="317b6-118">Первая команда использует Get-AzOperationalInsightsWorkspace для получения рабочей области MyWorkspace, а затем сохраняет ее в $Workspace переменной.</span><span class="sxs-lookup"><span data-stu-id="317b6-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="317b6-119">Вторая команда использует Get-AzStorageAccount для получения указанной учетной записи хранения, а затем сохраняет ее в $Storage переменной.</span><span class="sxs-lookup"><span data-stu-id="317b6-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="317b6-120">Третья команда передает учетную запись хранения в $Storage командлету Get-AzStorageAccountKey с помощью оператора конвейера для получения указанной клавиши, а затем сохраняет ее в переменной $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="317b6-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="317b6-121">В этом примере извлекется первый ключ.</span><span class="sxs-lookup"><span data-stu-id="317b6-121">This example retrieves the first key.</span></span> <span data-ttu-id="317b6-122">Чтобы получить другое значение, используйте значение[1] вместо value[0].</span><span class="sxs-lookup"><span data-stu-id="317b6-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="317b6-123">Конечная команда создает представление хранилища MyStorageInsight в рабочей области, определенной в $Workspace.</span><span class="sxs-lookup"><span data-stu-id="317b6-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="317b6-124">В таблице WADWindowsEventLogsTable в указанном ресурсе учетной записи хранилища данные расходуются.</span><span class="sxs-lookup"><span data-stu-id="317b6-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="317b6-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="317b6-125">PARAMETERS</span></span>

### <span data-ttu-id="317b6-126">-Containers</span><span class="sxs-lookup"><span data-stu-id="317b6-126">-Containers</span></span>
<span data-ttu-id="317b6-127">Определяет список контейнеров, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="317b6-127">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317b6-128">-DefaultProfile</span></span>
<span data-ttu-id="317b6-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="317b6-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="317b6-130">-Force</span><span class="sxs-lookup"><span data-stu-id="317b6-130">-Force</span></span>
<span data-ttu-id="317b6-131">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="317b6-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="317b6-132">-Name</span><span class="sxs-lookup"><span data-stu-id="317b6-132">-Name</span></span>
<span data-ttu-id="317b6-133">Указывает имя службы "Сведения о хранилище".</span><span class="sxs-lookup"><span data-stu-id="317b6-133">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317b6-134">-ResourceGroupName</span></span>
<span data-ttu-id="317b6-135">Имя группы ресурсов Azure, которая содержит рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="317b6-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="317b6-136">-StorageAccountKey</span></span>
<span data-ttu-id="317b6-137">Указывает ключ доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="317b6-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="317b6-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="317b6-139">Ресурс Azure для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="317b6-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="317b6-140">Это можно получить, выполив Get-AzStorageAccount и задав параметр *"Код"* результата.</span><span class="sxs-lookup"><span data-stu-id="317b6-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-141">-Таблицы</span><span class="sxs-lookup"><span data-stu-id="317b6-141">-Tables</span></span>
<span data-ttu-id="317b6-142">Определяет список таблиц, которые предоставляют данные.</span><span class="sxs-lookup"><span data-stu-id="317b6-142">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-143">-Workspace</span><span class="sxs-lookup"><span data-stu-id="317b6-143">-Workspace</span></span>
<span data-ttu-id="317b6-144">Определяет рабочее пространство для новой информации о хранилище.</span><span class="sxs-lookup"><span data-stu-id="317b6-144">Specifies the workspace for the new Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="317b6-145">-WorkspaceName</span></span>
<span data-ttu-id="317b6-146">Указывает имя существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="317b6-146">Specifies the name of an existing workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="317b6-147">-Confirm</span></span>
<span data-ttu-id="317b6-148">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="317b6-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="317b6-149">-WhatIf</span></span>
<span data-ttu-id="317b6-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="317b6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="317b6-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="317b6-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317b6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317b6-152">CommonParameters</span></span>
<span data-ttu-id="317b6-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="317b6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317b6-154">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317b6-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317b6-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="317b6-155">INPUTS</span></span>

### <span data-ttu-id="317b6-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="317b6-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="317b6-157">System.String</span><span class="sxs-lookup"><span data-stu-id="317b6-157">System.String</span></span>

### <span data-ttu-id="317b6-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="317b6-158">System.String[]</span></span>

## <span data-ttu-id="317b6-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="317b6-159">OUTPUTS</span></span>

### <span data-ttu-id="317b6-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="317b6-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="317b6-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="317b6-161">NOTES</span></span>

## <span data-ttu-id="317b6-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="317b6-162">RELATED LINKS</span></span>

[<span data-ttu-id="317b6-163">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="317b6-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="317b6-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="317b6-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


