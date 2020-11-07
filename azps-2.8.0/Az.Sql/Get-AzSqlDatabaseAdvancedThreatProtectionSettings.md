---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 186ff32138bba0556b05e9674f1711e9425a20c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906281"
---
# <span data-ttu-id="00177-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="00177-101">Get-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="00177-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00177-102">SYNOPSIS</span></span>
<span data-ttu-id="00177-103">Получает параметры расширенной защиты от угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="00177-103">Gets the advanced threat protection settings for a database.</span></span>

## <span data-ttu-id="00177-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00177-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvancedThreatProtectionSettings [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00177-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00177-105">DESCRIPTION</span></span>
<span data-ttu-id="00177-106">Командлет **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** получает расширенные параметры защиты от угроз для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="00177-106">The **Get-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL database.</span></span>
<span data-ttu-id="00177-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы определить базу данных, для которой этот командлет получает параметры.</span><span class="sxs-lookup"><span data-stu-id="00177-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="00177-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00177-108">EXAMPLES</span></span>

### <span data-ttu-id="00177-109">Пример 1: получение расширенных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="00177-109">Example 1: Get the advanced threat protection settings for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="00177-110">Эта команда получает расширенные параметры защиты от угроз для базы данных с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="00177-110">This command gets the advanced threat protection settings for a database named Database01.</span></span>
<span data-ttu-id="00177-111">База данных находится на сервере с именем Server01, который назначен группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="00177-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="00177-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00177-112">PARAMETERS</span></span>

### <span data-ttu-id="00177-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00177-113">-DatabaseName</span></span>
<span data-ttu-id="00177-114">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="00177-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="00177-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00177-115">-DefaultProfile</span></span>
<span data-ttu-id="00177-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="00177-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00177-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00177-117">-ResourceGroupName</span></span>
<span data-ttu-id="00177-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="00177-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="00177-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="00177-119">-ServerName</span></span>
<span data-ttu-id="00177-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="00177-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="00177-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00177-121">-Confirm</span></span>
<span data-ttu-id="00177-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00177-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00177-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00177-123">-WhatIf</span></span>
<span data-ttu-id="00177-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00177-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00177-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00177-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00177-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00177-126">CommonParameters</span></span>
<span data-ttu-id="00177-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00177-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00177-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00177-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00177-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00177-129">INPUTS</span></span>

### <span data-ttu-id="00177-130">System. String</span><span class="sxs-lookup"><span data-stu-id="00177-130">System.String</span></span>

## <span data-ttu-id="00177-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00177-131">OUTPUTS</span></span>

### <span data-ttu-id="00177-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="00177-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="00177-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="00177-133">NOTES</span></span>

## <span data-ttu-id="00177-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00177-134">RELATED LINKS</span></span>

[<span data-ttu-id="00177-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="00177-135">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)



