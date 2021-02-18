---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9035f2a03ac04a9bc99248c48675ab3c69b84207
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409619"
---
# <span data-ttu-id="d64ad-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="d64ad-101">Get-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="d64ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d64ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d64ad-103">Получает дополнительные параметры защиты от угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="d64ad-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="d64ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d64ad-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSetting [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d64ad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d64ad-105">DESCRIPTION</span></span>
<span data-ttu-id="d64ad-106">Для получения дополнительных параметров защиты от угроз в базе данных Azure SQL параметры защиты от **угрозыAdvancedThreatProtectionSetting Get-AzSqlDatabaseAdvancedThreatProtectionSetting.**</span><span class="sxs-lookup"><span data-stu-id="d64ad-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="d64ad-107">Чтобы использовать этот cmdlet, укажите параметры *ResourceGroupName,* *ServerName* и *DatabaseName,* чтобы определить базу данных, для которой этот cmdlet получает параметры.</span><span class="sxs-lookup"><span data-stu-id="d64ad-107">To use this cmdlet, specify the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="d64ad-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d64ad-108">EXAMPLES</span></span>

### <span data-ttu-id="d64ad-109">Пример 1. Расширенные параметры защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="d64ad-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="d64ad-110">Эта команда получает расширенные параметры защиты от угроз для базы данных с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="d64ad-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="d64ad-111">База данных расположена на сервере Server01, который назначен группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d64ad-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d64ad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d64ad-112">PARAMETERS</span></span>

### <span data-ttu-id="d64ad-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d64ad-113">-DatabaseName</span></span>
<span data-ttu-id="d64ad-114">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d64ad-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="d64ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64ad-115">-DefaultProfile</span></span>
<span data-ttu-id="d64ad-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d64ad-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d64ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d64ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="d64ad-118">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="d64ad-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d64ad-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d64ad-119">-ServerName</span></span>
<span data-ttu-id="d64ad-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d64ad-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="d64ad-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d64ad-121">-Confirm</span></span>
<span data-ttu-id="d64ad-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d64ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d64ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64ad-123">-WhatIf</span></span>
<span data-ttu-id="d64ad-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d64ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d64ad-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d64ad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d64ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64ad-126">CommonParameters</span></span>
<span data-ttu-id="d64ad-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64ad-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d64ad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64ad-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d64ad-129">INPUTS</span></span>

### <span data-ttu-id="d64ad-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d64ad-130">System.String</span></span>

## <span data-ttu-id="d64ad-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d64ad-131">OUTPUTS</span></span>

### <span data-ttu-id="d64ad-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="d64ad-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="d64ad-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d64ad-133">NOTES</span></span>

## <span data-ttu-id="d64ad-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d64ad-134">RELATED LINKS</span></span>




