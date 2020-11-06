---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 1bea5ce9eda22996eb65b6e5d26fb3af19cd1c88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562751"
---
# <span data-ttu-id="45d2e-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="45d2e-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="45d2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="45d2e-103">Создает представление хранилища в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="45d2e-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45d2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45d2e-104">SYNTAX</span></span>

### <span data-ttu-id="45d2e-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45d2e-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45d2e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="45d2e-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45d2e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45d2e-107">DESCRIPTION</span></span>
<span data-ttu-id="45d2e-108">Командлет **New-AzureRmOperationalInsightsStorageInsight** создает новое представление хранилища в существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="45d2e-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="45d2e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45d2e-109">EXAMPLES</span></span>

### <span data-ttu-id="45d2e-110">Пример 1: создание аналитического хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="45d2e-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="45d2e-111">Первая команда использует командлет Get-AzureRmStorageAccount для получения учетной записи хранения с именем ContosoStorage, а затем сохраняет ее в переменной $Storage.</span><span class="sxs-lookup"><span data-stu-id="45d2e-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="45d2e-112">Вторая команда передает учетную запись хранения в $Storage командлету Get-AzureRmStorageAccountKey с помощью оператора конвейера для получения указанного ключа учетной записи хранения, а затем сохраняет его в переменной $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="45d2e-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="45d2e-113">Последняя команда создает аналитическое представление хранилища с именем MyStorageInsight в рабочей области с именем MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="45d2e-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="45d2e-114">Это аналитическое хранилище потребляет данные из таблицы WADWindowsEventLogsTable в указанном ресурсе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="45d2e-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="45d2e-115">Пример 2: создание аналитического элемента хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="45d2e-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="45d2e-116">Первая команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем сохранит ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="45d2e-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="45d2e-117">Вторая команда использует командлет Get-AzureRmStorageAccount, чтобы получить указанную учетную запись хранения, а затем сохранит ее в переменной $Storage.</span><span class="sxs-lookup"><span data-stu-id="45d2e-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="45d2e-118">Третья команда передает учетную запись хранения в $Storage командлету Get-AzureRmStorageAccountKey с помощью оператора конвейера для получения указанного ключа, а затем сохраняет его в переменной $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="45d2e-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="45d2e-119">Последняя команда создает аналитическое представление хранилища с именем MyStorageInsight в рабочей области, определенной в $Workspace.</span><span class="sxs-lookup"><span data-stu-id="45d2e-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="45d2e-120">Аналитика хранилища потребляет данные из таблицы WADWindowsEventLogsTable в указанном ресурсе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="45d2e-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="45d2e-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45d2e-121">PARAMETERS</span></span>

### <span data-ttu-id="45d2e-122">-Containers</span><span class="sxs-lookup"><span data-stu-id="45d2e-122">-Containers</span></span>
<span data-ttu-id="45d2e-123">Указывает список контейнеров, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="45d2e-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="45d2e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d2e-124">-DefaultProfile</span></span>
<span data-ttu-id="45d2e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="45d2e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45d2e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="45d2e-126">-Force</span></span>
<span data-ttu-id="45d2e-127">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="45d2e-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45d2e-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45d2e-128">-Name</span></span>
<span data-ttu-id="45d2e-129">Указывает имя аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="45d2e-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="45d2e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d2e-130">-ResourceGroupName</span></span>
<span data-ttu-id="45d2e-131">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="45d2e-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="45d2e-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="45d2e-132">-StorageAccountKey</span></span>
<span data-ttu-id="45d2e-133">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="45d2e-133">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="45d2e-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="45d2e-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="45d2e-135">Указывает ресурс Azure учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="45d2e-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="45d2e-136">Это можно получить, выполнив командлет Get-AzureRmStorageAccount и обратившись к параметру *ID* результата.</span><span class="sxs-lookup"><span data-stu-id="45d2e-136">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="45d2e-137">-Таблицы</span><span class="sxs-lookup"><span data-stu-id="45d2e-137">-Tables</span></span>
<span data-ttu-id="45d2e-138">Указывает список таблиц, предоставляющих данные.</span><span class="sxs-lookup"><span data-stu-id="45d2e-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="45d2e-139">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="45d2e-139">-Workspace</span></span>
<span data-ttu-id="45d2e-140">Указывает рабочую область для нового аналитического хранилища.</span><span class="sxs-lookup"><span data-stu-id="45d2e-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="45d2e-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="45d2e-141">-WorkspaceName</span></span>
<span data-ttu-id="45d2e-142">Указывает имя существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="45d2e-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="45d2e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45d2e-143">-Confirm</span></span>
<span data-ttu-id="45d2e-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45d2e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d2e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d2e-145">-WhatIf</span></span>
<span data-ttu-id="45d2e-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45d2e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45d2e-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45d2e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d2e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d2e-148">CommonParameters</span></span>
<span data-ttu-id="45d2e-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45d2e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d2e-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d2e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d2e-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45d2e-151">INPUTS</span></span>

### <span data-ttu-id="45d2e-152">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="45d2e-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="45d2e-153">Параметры: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45d2e-153">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="45d2e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="45d2e-154">System.String</span></span>

### <span data-ttu-id="45d2e-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="45d2e-155">System.String[]</span></span>

## <span data-ttu-id="45d2e-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45d2e-156">OUTPUTS</span></span>

### <span data-ttu-id="45d2e-157">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="45d2e-157">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="45d2e-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="45d2e-158">NOTES</span></span>

## <span data-ttu-id="45d2e-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45d2e-159">RELATED LINKS</span></span>

[<span data-ttu-id="45d2e-160">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="45d2e-160">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="45d2e-161">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="45d2e-161">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


