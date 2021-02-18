---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231841"
---
# <span data-ttu-id="fa2e0-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="fa2e0-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="fa2e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="fa2e0-103">Возвращает SQL базы данных для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="fa2e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa2e0-104">SYNTAX</span></span>

### <span data-ttu-id="fa2e0-105">FilterResults (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa2e0-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa2e0-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="fa2e0-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa2e0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa2e0-107">DESCRIPTION</span></span>
<span data-ttu-id="fa2e0-108">С **его использованием** можно получить возможности azure SQL Database, доступные в текущей подписке для региона.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="fa2e0-109">Если указать *параметры ServerVersionName,* *EditionName* или *ServiceObjectiveName, этот cmdlet* возвратит указанные значения и их предшественники.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-109">If you specify the *ServerVersionName*, *EditionName*, or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="fa2e0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa2e0-110">EXAMPLES</span></span>

### <span data-ttu-id="fa2e0-111">Пример 1. Получить возможности для текущей подписки для региона</span><span class="sxs-lookup"><span data-stu-id="fa2e0-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="fa2e0-112">Эта команда возвращает возможности экземпляров SQL базы данных в текущей подписке для центрального региона США.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="fa2e0-113">Пример 2. Получить возможности по умолчанию для текущей подписки для региона</span><span class="sxs-lookup"><span data-stu-id="fa2e0-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="fa2e0-114">Эта команда возвращает возможности по умолчанию для SQL баз данных в текущей подписке в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="fa2e0-115">Пример 3. Подробные сведения о цели обслуживания</span><span class="sxs-lookup"><span data-stu-id="fa2e0-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="fa2e0-116">Эта команда получает возможности по умолчанию для SQL баз данных для указанной цели обслуживания в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="fa2e0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa2e0-117">PARAMETERS</span></span>

### <span data-ttu-id="fa2e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa2e0-118">-DefaultProfile</span></span>
<span data-ttu-id="fa2e0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fa2e0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa2e0-120">-Defaults</span><span class="sxs-lookup"><span data-stu-id="fa2e0-120">-Defaults</span></span>
<span data-ttu-id="fa2e0-121">Указывает на то, что этот cmdlet получает только значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-121">Indicates that this cmdlet gets only defaults.</span></span>

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

### <span data-ttu-id="fa2e0-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="fa2e0-122">-EditionName</span></span>
<span data-ttu-id="fa2e0-123">Название выпуска базы данных, для которого этот cmdlet получает возможности.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="fa2e0-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="fa2e0-124">-LocationName</span></span>
<span data-ttu-id="fa2e0-125">Указывает имя расположения, для которого этот cmdlet получает возможности.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="fa2e0-126">Дополнительные сведения см. в области Azure http://azure.microsoft.com/en-us/regions/ ( http://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="fa2e0-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="fa2e0-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="fa2e0-127">-ServerVersionName</span></span>
<span data-ttu-id="fa2e0-128">Указывает имя версии сервера, для которой этот cmdlet получает возможности.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="fa2e0-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="fa2e0-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="fa2e0-130">Указывает имя цели обслуживания, для которой этот cmdlet получает возможности.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="fa2e0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa2e0-131">-Confirm</span></span>
<span data-ttu-id="fa2e0-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa2e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa2e0-133">-WhatIf</span></span>
<span data-ttu-id="fa2e0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa2e0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa2e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa2e0-136">CommonParameters</span></span>
<span data-ttu-id="fa2e0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa2e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa2e0-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa2e0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa2e0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa2e0-139">INPUTS</span></span>

### <span data-ttu-id="fa2e0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fa2e0-140">System.String</span></span>

## <span data-ttu-id="fa2e0-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa2e0-141">OUTPUTS</span></span>

### <span data-ttu-id="fa2e0-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="fa2e0-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="fa2e0-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa2e0-143">NOTES</span></span>

## <span data-ttu-id="fa2e0-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa2e0-144">RELATED LINKS</span></span>
