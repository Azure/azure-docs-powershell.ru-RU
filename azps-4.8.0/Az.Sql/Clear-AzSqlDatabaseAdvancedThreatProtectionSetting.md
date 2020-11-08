---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078723"
---
# <span data-ttu-id="357bb-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="357bb-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="357bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="357bb-102">SYNOPSIS</span></span>
<span data-ttu-id="357bb-103">Удаление расширенных параметров защиты от угроз из базы данных.</span><span class="sxs-lookup"><span data-stu-id="357bb-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="357bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="357bb-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="357bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="357bb-105">DESCRIPTION</span></span>
<span data-ttu-id="357bb-106">Командлет **clear-AzSqlDatabaseAdvancedThreatProtectionSetting** удаляет расширенные параметры защиты от угроз из базы данных SQL AzureAzure.</span><span class="sxs-lookup"><span data-stu-id="357bb-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="357bb-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* , чтобы определить базу данных, из которой этот командлет удаляет параметры.</span><span class="sxs-lookup"><span data-stu-id="357bb-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="357bb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="357bb-108">EXAMPLES</span></span>

### <span data-ttu-id="357bb-109">Пример 1: Удаление расширенных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="357bb-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="357bb-110">Эта команда удаляет расширенные параметры защиты от угроз из базы данных с именем Database01 на сервере под названием Server01.</span><span class="sxs-lookup"><span data-stu-id="357bb-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="357bb-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="357bb-111">PARAMETERS</span></span>

### <span data-ttu-id="357bb-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="357bb-112">-DatabaseName</span></span>
<span data-ttu-id="357bb-113">Указывает имя базы данных, в которой должны быть удалены дополнительные параметры защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="357bb-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="357bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357bb-114">-DefaultProfile</span></span>
<span data-ttu-id="357bb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="357bb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="357bb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="357bb-116">-PassThru</span></span>
<span data-ttu-id="357bb-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="357bb-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="357bb-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="357bb-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="357bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="357bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="357bb-120">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="357bb-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="357bb-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="357bb-121">-ServerName</span></span>
<span data-ttu-id="357bb-122">Указывает имя сервера, на котором работает база данных.</span><span class="sxs-lookup"><span data-stu-id="357bb-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="357bb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="357bb-123">-Confirm</span></span>
<span data-ttu-id="357bb-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="357bb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="357bb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="357bb-125">-WhatIf</span></span>
<span data-ttu-id="357bb-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="357bb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="357bb-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="357bb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="357bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357bb-128">CommonParameters</span></span>
<span data-ttu-id="357bb-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="357bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357bb-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="357bb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357bb-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="357bb-131">INPUTS</span></span>

### <span data-ttu-id="357bb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="357bb-132">System.String</span></span>

## <span data-ttu-id="357bb-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="357bb-133">OUTPUTS</span></span>

### <span data-ttu-id="357bb-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="357bb-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="357bb-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="357bb-135">NOTES</span></span>

## <span data-ttu-id="357bb-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="357bb-136">RELATED LINKS</span></span>

[<span data-ttu-id="357bb-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="357bb-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


