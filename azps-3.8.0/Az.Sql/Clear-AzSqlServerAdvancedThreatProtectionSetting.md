---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073699"
---
# <span data-ttu-id="2e138-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="2e138-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="2e138-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e138-102">SYNOPSIS</span></span>
<span data-ttu-id="2e138-103">Удаление дополнительных параметров защиты от угроз с сервера.</span><span class="sxs-lookup"><span data-stu-id="2e138-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="2e138-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e138-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e138-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e138-105">DESCRIPTION</span></span>
<span data-ttu-id="2e138-106">Командлет Clear-AzSqlServerAdvancedThreatProtectionSetting удаляет расширенные параметры защиты от угроз с сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2e138-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="2e138-107">Чтобы использовать этот командлет, укажите параметры ResourceGroupName и ServerName для идентификации сервера, с которого этот командлет удаляет параметры.</span><span class="sxs-lookup"><span data-stu-id="2e138-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="2e138-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e138-108">EXAMPLES</span></span>

### <span data-ttu-id="2e138-109">Пример 1: Удаление расширенных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="2e138-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="2e138-110">Эта команда удаляет расширенные параметры защиты от угроз с сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="2e138-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="2e138-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e138-111">PARAMETERS</span></span>

### <span data-ttu-id="2e138-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e138-112">-DefaultProfile</span></span>
<span data-ttu-id="2e138-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2e138-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e138-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e138-114">-PassThru</span></span>
<span data-ttu-id="2e138-115">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2e138-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e138-116">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2e138-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e138-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e138-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e138-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="2e138-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="2e138-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2e138-119">-ServerName</span></span>
<span data-ttu-id="2e138-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2e138-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e138-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e138-121">-Confirm</span></span>
<span data-ttu-id="2e138-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e138-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e138-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e138-123">-WhatIf</span></span>
<span data-ttu-id="2e138-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e138-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e138-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e138-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e138-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e138-126">CommonParameters</span></span>
<span data-ttu-id="2e138-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e138-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e138-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e138-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e138-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e138-129">INPUTS</span></span>

### <span data-ttu-id="2e138-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2e138-130">System.String</span></span>

## <span data-ttu-id="2e138-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e138-131">OUTPUTS</span></span>

### <span data-ttu-id="2e138-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="2e138-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="2e138-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e138-133">NOTES</span></span>

## <span data-ttu-id="2e138-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e138-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e138-135">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2e138-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

