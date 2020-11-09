---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlCapability.md
ms.openlocfilehash: 582b512ef502e0dac3fc443807f1e33a65063728
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246709"
---
# <span data-ttu-id="1f12f-101">Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="1f12f-101">Get-AzSqlCapability</span></span>

## <span data-ttu-id="1f12f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f12f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f12f-103">Возвращает возможности базы данных SQL для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="1f12f-103">Gets SQL Database capabilities for the current subscription.</span></span>

## <span data-ttu-id="1f12f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f12f-104">SYNTAX</span></span>

### <span data-ttu-id="1f12f-105">FilterResults (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f12f-105">FilterResults (Default)</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f12f-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="1f12f-106">DefaultResults</span></span>
```
Get-AzSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f12f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f12f-107">DESCRIPTION</span></span>
<span data-ttu-id="1f12f-108">Командлет **Get-AzSqlCapability** получает возможности базы данных SQL Azure, доступные в текущей подписке для региона.</span><span class="sxs-lookup"><span data-stu-id="1f12f-108">The **Get-AzSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="1f12f-109">Если заданы параметры *ServerVersionName* , *EditionName* или *ServiceObjectiveName* , этот командлет возвращает указанные значения и их предшественники.</span><span class="sxs-lookup"><span data-stu-id="1f12f-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="1f12f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f12f-110">EXAMPLES</span></span>

### <span data-ttu-id="1f12f-111">Пример 1: получение возможностей для текущей подписки для региона</span><span class="sxs-lookup"><span data-stu-id="1f12f-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="1f12f-112">Эта команда возвращает возможности для экземпляров базы данных SQL в текущей подписке для центрального региона США.</span><span class="sxs-lookup"><span data-stu-id="1f12f-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="1f12f-113">Пример 2: получение возможностей по умолчанию для текущей подписки для региона</span><span class="sxs-lookup"><span data-stu-id="1f12f-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="1f12f-114">Эта команда возвращает возможности по умолчанию для баз данных SQL в текущей подписке в центральном регионе США.</span><span class="sxs-lookup"><span data-stu-id="1f12f-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="1f12f-115">Пример 3: получение сведений о цели обслуживания</span><span class="sxs-lookup"><span data-stu-id="1f12f-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="1f12f-116">Эта команда получает возможности по умолчанию для баз данных SQL для указанной цели обслуживания в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="1f12f-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="1f12f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f12f-117">PARAMETERS</span></span>

### <span data-ttu-id="1f12f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f12f-118">-DefaultProfile</span></span>
<span data-ttu-id="1f12f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f12f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f12f-120">-Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1f12f-120">-Defaults</span></span>
<span data-ttu-id="1f12f-121">Указывает на то, что этот командлет получает только значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f12f-121">Indicates that this cmdlet gets only defaults.</span></span>

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

### <span data-ttu-id="1f12f-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="1f12f-122">-EditionName</span></span>
<span data-ttu-id="1f12f-123">Указывает имя выпуска базы данных, для которого этот командлет получает возможности.</span><span class="sxs-lookup"><span data-stu-id="1f12f-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="1f12f-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="1f12f-124">-LocationName</span></span>
<span data-ttu-id="1f12f-125">Указывает имя расположения, для которого этот командлет получает возможности.</span><span class="sxs-lookup"><span data-stu-id="1f12f-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="1f12f-126">Дополнительные сведения можно найти в разделе регионы Azure http://azure.microsoft.com/en-us/regions/ ( http://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="1f12f-126">For more information, see Azure Regionshttp://azure.microsoft.com/en-us/regions/ (http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="1f12f-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="1f12f-127">-ServerVersionName</span></span>
<span data-ttu-id="1f12f-128">Указывает имя серверной версии, для которой этот командлет получает возможности.</span><span class="sxs-lookup"><span data-stu-id="1f12f-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="1f12f-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1f12f-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="1f12f-130">Указывает имя цели обслуживания, к которой этот командлет получает возможности.</span><span class="sxs-lookup"><span data-stu-id="1f12f-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

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

### <span data-ttu-id="1f12f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f12f-131">-Confirm</span></span>
<span data-ttu-id="1f12f-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f12f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f12f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f12f-133">-WhatIf</span></span>
<span data-ttu-id="1f12f-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f12f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f12f-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f12f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f12f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f12f-136">CommonParameters</span></span>
<span data-ttu-id="1f12f-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f12f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f12f-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f12f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f12f-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f12f-139">INPUTS</span></span>

### <span data-ttu-id="1f12f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1f12f-140">System.String</span></span>

## <span data-ttu-id="1f12f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f12f-141">OUTPUTS</span></span>

### <span data-ttu-id="1f12f-142">Microsoft.Azure.Commands.Sql.Location_Capabilities. Model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="1f12f-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="1f12f-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f12f-143">NOTES</span></span>

## <span data-ttu-id="1f12f-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f12f-144">RELATED LINKS</span></span>