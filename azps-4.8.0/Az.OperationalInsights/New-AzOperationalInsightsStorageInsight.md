---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079415"
---
# <span data-ttu-id="3ded9-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="3ded9-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="3ded9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ded9-102">SYNOPSIS</span></span>
<span data-ttu-id="3ded9-103">Создает представление хранилища в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3ded9-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="3ded9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ded9-104">SYNTAX</span></span>

### <span data-ttu-id="3ded9-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ded9-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ded9-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3ded9-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ded9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ded9-107">DESCRIPTION</span></span>
<span data-ttu-id="3ded9-108">Командлет **New-AzOperationalInsightsStorageInsight** создает новое представление хранилища в существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3ded9-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="3ded9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ded9-109">EXAMPLES</span></span>

### <span data-ttu-id="3ded9-110">Пример 1: создание аналитического хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="3ded9-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="3ded9-111">Первая команда использует командлет Get-AzStorageAccount для получения учетной записи хранения с именем ContosoStorage, а затем сохраняет ее в переменной $Storage.</span><span class="sxs-lookup"><span data-stu-id="3ded9-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="3ded9-112">Вторая команда передает учетную запись хранения в $Storage командлету Get-AzStorageAccountKey с помощью оператора конвейера для получения указанного ключа учетной записи хранения, а затем сохраняет его в переменной $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="3ded9-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="3ded9-113">В этом примере извлекается первый ключ.</span><span class="sxs-lookup"><span data-stu-id="3ded9-113">This example retrieves the first key.</span></span> <span data-ttu-id="3ded9-114">Чтобы получить другой, используйте значение [1] вместо значения [0].</span><span class="sxs-lookup"><span data-stu-id="3ded9-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="3ded9-115">Последняя команда создает аналитическое представление хранилища с именем MyStorageInsight в рабочей области с именем MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3ded9-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="3ded9-116">Это аналитическое хранилище потребляет данные из таблицы WADWindowsEventLogsTable в указанном ресурсе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3ded9-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="3ded9-117">Пример 2: создание аналитического элемента хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="3ded9-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="3ded9-118">Первая команда использует командлет Get-AzOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем сохранит ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="3ded9-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="3ded9-119">Вторая команда использует командлет Get-AzStorageAccount, чтобы получить указанную учетную запись хранения, а затем сохранит ее в переменной $Storage.</span><span class="sxs-lookup"><span data-stu-id="3ded9-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="3ded9-120">Третья команда передает учетную запись хранения в $Storage командлету Get-AzStorageAccountKey с помощью оператора конвейера для получения указанного ключа, а затем сохраняет его в переменной $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="3ded9-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="3ded9-121">В этом примере извлекается первый ключ.</span><span class="sxs-lookup"><span data-stu-id="3ded9-121">This example retrieves the first key.</span></span> <span data-ttu-id="3ded9-122">Чтобы получить другой, используйте значение [1] вместо значения [0].</span><span class="sxs-lookup"><span data-stu-id="3ded9-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="3ded9-123">Последняя команда создает аналитическое представление хранилища с именем MyStorageInsight в рабочей области, определенной в $Workspace.</span><span class="sxs-lookup"><span data-stu-id="3ded9-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="3ded9-124">Аналитика хранилища потребляет данные из таблицы WADWindowsEventLogsTable в указанном ресурсе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3ded9-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="3ded9-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ded9-125">PARAMETERS</span></span>

### <span data-ttu-id="3ded9-126">-Containers</span><span class="sxs-lookup"><span data-stu-id="3ded9-126">-Containers</span></span>
<span data-ttu-id="3ded9-127">Указывает список контейнеров, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="3ded9-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="3ded9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ded9-128">-DefaultProfile</span></span>
<span data-ttu-id="3ded9-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3ded9-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ded9-130">-Force</span><span class="sxs-lookup"><span data-stu-id="3ded9-130">-Force</span></span>
<span data-ttu-id="3ded9-131">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ded9-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ded9-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ded9-132">-Name</span></span>
<span data-ttu-id="3ded9-133">Указывает имя аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ded9-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="3ded9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ded9-134">-ResourceGroupName</span></span>
<span data-ttu-id="3ded9-135">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="3ded9-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3ded9-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3ded9-136">-StorageAccountKey</span></span>
<span data-ttu-id="3ded9-137">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3ded9-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="3ded9-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3ded9-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="3ded9-139">Указывает ресурс Azure учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3ded9-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="3ded9-140">Это можно получить, выполнив командлет Get-AzStorageAccount и обратившись к параметру *ID* результата.</span><span class="sxs-lookup"><span data-stu-id="3ded9-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="3ded9-141">-Таблицы</span><span class="sxs-lookup"><span data-stu-id="3ded9-141">-Tables</span></span>
<span data-ttu-id="3ded9-142">Указывает список таблиц, предоставляющих данные.</span><span class="sxs-lookup"><span data-stu-id="3ded9-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="3ded9-143">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="3ded9-143">-Workspace</span></span>
<span data-ttu-id="3ded9-144">Указывает рабочую область для нового аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="3ded9-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="3ded9-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ded9-145">-WorkspaceName</span></span>
<span data-ttu-id="3ded9-146">Указывает имя существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3ded9-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="3ded9-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ded9-147">-Confirm</span></span>
<span data-ttu-id="3ded9-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ded9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ded9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ded9-149">-WhatIf</span></span>
<span data-ttu-id="3ded9-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ded9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ded9-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ded9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ded9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ded9-152">CommonParameters</span></span>
<span data-ttu-id="3ded9-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ded9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ded9-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ded9-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ded9-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ded9-155">INPUTS</span></span>

### <span data-ttu-id="3ded9-156">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ded9-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3ded9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3ded9-157">System.String</span></span>

### <span data-ttu-id="3ded9-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="3ded9-158">System.String[]</span></span>

## <span data-ttu-id="3ded9-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ded9-159">OUTPUTS</span></span>

### <span data-ttu-id="3ded9-160">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="3ded9-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="3ded9-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ded9-161">NOTES</span></span>

## <span data-ttu-id="3ded9-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ded9-162">RELATED LINKS</span></span>

[<span data-ttu-id="3ded9-163">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="3ded9-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="3ded9-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ded9-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


