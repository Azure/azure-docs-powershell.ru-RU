---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399935"
---
# <span data-ttu-id="41b96-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="41b96-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="41b96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41b96-102">SYNOPSIS</span></span>
<span data-ttu-id="41b96-103">Возвращает SQL базы данных для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="41b96-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="41b96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41b96-104">SYNTAX</span></span>

### <span data-ttu-id="41b96-105">FilterResults (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41b96-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41b96-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="41b96-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41b96-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41b96-107">DESCRIPTION</span></span>
<span data-ttu-id="41b96-108">С **его использованием** можно получить возможности azure SQL Database, доступные в текущей подписке для региона.</span><span class="sxs-lookup"><span data-stu-id="41b96-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="41b96-109">Если указать *параметры ServerVersionName,* *EditionName* или *ServiceObjectiveName, этот cmdlet* возвратит указанные значения и их предшественники.</span><span class="sxs-lookup"><span data-stu-id="41b96-109">If you specify the *ServerVersionName*, *EditionName*, or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="41b96-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41b96-110">EXAMPLES</span></span>

### <span data-ttu-id="41b96-111">Пример 1. Получить возможности для текущей подписки для региона</span><span class="sxs-lookup"><span data-stu-id="41b96-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="41b96-112">Эта команда возвращает возможности экземпляров SQL базы данных в текущей подписке для центрального региона США.</span><span class="sxs-lookup"><span data-stu-id="41b96-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="41b96-113">Пример 2. Получить возможности по умолчанию для текущей подписки для региона</span><span class="sxs-lookup"><span data-stu-id="41b96-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="41b96-114">Эта команда возвращает возможности по умолчанию для SQL баз данных в текущей подписке в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="41b96-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="41b96-115">Пример 3. Подробные сведения о цели обслуживания</span><span class="sxs-lookup"><span data-stu-id="41b96-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="41b96-116">Эта команда по умолчанию может SQL базы данных для указанной цели обслуживания по текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="41b96-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="41b96-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41b96-117">PARAMETERS</span></span>

### <span data-ttu-id="41b96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b96-118">-DefaultProfile</span></span>
<span data-ttu-id="41b96-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="41b96-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41b96-120">-Defaults</span><span class="sxs-lookup"><span data-stu-id="41b96-120">-Defaults</span></span>
<span data-ttu-id="41b96-121">Указывает на то, что этот cmdlet получает только значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41b96-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="41b96-122">-EditionName</span></span>
<span data-ttu-id="41b96-123">Название выпуска базы данных, для которого этот cmdlet получает возможности.</span><span class="sxs-lookup"><span data-stu-id="41b96-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="41b96-124">-LocationName</span></span>
<span data-ttu-id="41b96-125">Указывает имя расположения, для которого этот cmdlet получает возможности.</span><span class="sxs-lookup"><span data-stu-id="41b96-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="41b96-126">Дополнительные сведения см. в области Azure http://azure.microsoft.com/en-us/regions/ ( http://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="41b96-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="41b96-127">-ServerVersionName</span></span>
<span data-ttu-id="41b96-128">Указывает имя версии сервера, для которой этот cmdlet получает возможности.</span><span class="sxs-lookup"><span data-stu-id="41b96-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="41b96-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="41b96-130">Указывает имя цели обслуживания, для которой этот cmdlet получает возможности.</span><span class="sxs-lookup"><span data-stu-id="41b96-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b96-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41b96-131">-Confirm</span></span>
<span data-ttu-id="41b96-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="41b96-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41b96-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b96-133">-WhatIf</span></span>
<span data-ttu-id="41b96-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41b96-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41b96-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="41b96-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41b96-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b96-136">CommonParameters</span></span>
<span data-ttu-id="41b96-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41b96-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b96-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41b96-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b96-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41b96-139">INPUTS</span></span>

### <span data-ttu-id="41b96-140">System.String</span><span class="sxs-lookup"><span data-stu-id="41b96-140">System.String</span></span>

## <span data-ttu-id="41b96-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41b96-141">OUTPUTS</span></span>

### <span data-ttu-id="41b96-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="41b96-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="41b96-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41b96-143">NOTES</span></span>

## <span data-ttu-id="41b96-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41b96-144">RELATED LINKS</span></span>
