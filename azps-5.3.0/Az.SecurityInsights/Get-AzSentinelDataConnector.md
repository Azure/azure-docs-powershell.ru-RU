---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517585"
---
# <span data-ttu-id="03ca0-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="03ca0-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="03ca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="03ca0-103">"Получить соединители данных".</span><span class="sxs-lookup"><span data-stu-id="03ca0-103">Get a Data Connector.</span></span>

## <span data-ttu-id="03ca0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="03ca0-104">SYNTAX</span></span>

### <span data-ttu-id="03ca0-105">WorkspaceScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03ca0-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03ca0-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="03ca0-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03ca0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="03ca0-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03ca0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03ca0-108">DESCRIPTION</span></span>
<span data-ttu-id="03ca0-109">**Cmdlet Get-AzSentinelDataConnector** получает соединитель данных из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="03ca0-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="03ca0-110">Если задать параметр *DataConnectorId,* возвращается один объект **DataConnector.**</span><span class="sxs-lookup"><span data-stu-id="03ca0-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="03ca0-111">Если параметр *DataConnectorId* не задан, возвращается массив, содержащий все соединители данных в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="03ca0-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="03ca0-112">Для обновления соединитетеля данных можно использовать объект **DataConnector(** например, отключить **его).**</span><span class="sxs-lookup"><span data-stu-id="03ca0-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="03ca0-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="03ca0-113">EXAMPLES</span></span>

### <span data-ttu-id="03ca0-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="03ca0-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="03ca0-115">В этом примере все **dataConnectors в** указанной рабочей области получаются, а затем $DataConnectors переменной.</span><span class="sxs-lookup"><span data-stu-id="03ca0-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="03ca0-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="03ca0-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="03ca0-117">В этом примере **dataConnector в** указанной рабочей области хранится в переменной $DataConnector данных.</span><span class="sxs-lookup"><span data-stu-id="03ca0-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="03ca0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03ca0-118">PARAMETERS</span></span>

### <span data-ttu-id="03ca0-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="03ca0-119">-DataConnectorId</span></span>
<span data-ttu-id="03ca0-120">Data Connector Id.</span><span class="sxs-lookup"><span data-stu-id="03ca0-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ca0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ca0-121">-DefaultProfile</span></span>
<span data-ttu-id="03ca0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03ca0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03ca0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ca0-123">-ResourceGroupName</span></span>
<span data-ttu-id="03ca0-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03ca0-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ca0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03ca0-125">-ResourceId</span></span>
<span data-ttu-id="03ca0-126">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="03ca0-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ca0-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03ca0-127">-WorkspaceName</span></span>
<span data-ttu-id="03ca0-128">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="03ca0-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ca0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ca0-129">CommonParameters</span></span>
<span data-ttu-id="03ca0-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ca0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ca0-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03ca0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ca0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03ca0-132">INPUTS</span></span>

### <span data-ttu-id="03ca0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="03ca0-133">System.String</span></span>
## <span data-ttu-id="03ca0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03ca0-134">OUTPUTS</span></span>

### <span data-ttu-id="03ca0-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="03ca0-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="03ca0-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="03ca0-136">NOTES</span></span>

## <span data-ttu-id="03ca0-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03ca0-137">RELATED LINKS</span></span>
