---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410287"
---
# <span data-ttu-id="0d8fe-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="0d8fe-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="0d8fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8fe-103">Удаляет дополнительные параметры защиты от угроз из базы данных.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="0d8fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0d8fe-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d8fe-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d8fe-105">DESCRIPTION</span></span>
<span data-ttu-id="0d8fe-106">Для **этого** из базы данных AzureAzure SQL расширенные параметры защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="0d8fe-107">Чтобы использовать этот cmdlet, укажите параметры *ResourceGroupName* и *ServerName,* чтобы определить базу данных, из которой этот cmdlet удаляет параметры.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="0d8fe-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0d8fe-108">EXAMPLES</span></span>

### <span data-ttu-id="0d8fe-109">Пример 1. Удаление дополнительных параметров защиты от угроз в базе данных</span><span class="sxs-lookup"><span data-stu-id="0d8fe-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="0d8fe-110">Эта команда удаляет дополнительные параметры защиты от угроз из базы данных Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="0d8fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d8fe-111">PARAMETERS</span></span>

### <span data-ttu-id="0d8fe-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d8fe-112">-DatabaseName</span></span>
<span data-ttu-id="0d8fe-113">Имя базы данных, для которой необходимо удалить дополнительные параметры защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8fe-114">-DefaultProfile</span></span>
<span data-ttu-id="0d8fe-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0d8fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d8fe-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d8fe-116">-PassThru</span></span>
<span data-ttu-id="0d8fe-117">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d8fe-118">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d8fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d8fe-120">Имя группы ресурсов, которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="0d8fe-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0d8fe-121">-ServerName</span></span>
<span data-ttu-id="0d8fe-122">Указывает имя сервера, на котором работает база данных.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-122">Specifies the name of a server on which the database runs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8fe-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d8fe-123">-Confirm</span></span>
<span data-ttu-id="0d8fe-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d8fe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d8fe-125">-WhatIf</span></span>
<span data-ttu-id="0d8fe-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d8fe-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d8fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8fe-128">CommonParameters</span></span>
<span data-ttu-id="0d8fe-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d8fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8fe-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d8fe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8fe-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d8fe-131">INPUTS</span></span>

### <span data-ttu-id="0d8fe-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0d8fe-132">System.String</span></span>

## <span data-ttu-id="0d8fe-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d8fe-133">OUTPUTS</span></span>

### <span data-ttu-id="0d8fe-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="0d8fe-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="0d8fe-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0d8fe-135">NOTES</span></span>

## <span data-ttu-id="0d8fe-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d8fe-136">RELATED LINKS</span></span>

[<span data-ttu-id="0d8fe-137">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="0d8fe-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

