---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 1895fe45f51782cc1a3a54d8b2d0f2da752c2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906098"
---
# <span data-ttu-id="af7a6-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="af7a6-101">Get-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="af7a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="af7a6-103">Получает параметры расширенной защиты от угроз для сервера.</span><span class="sxs-lookup"><span data-stu-id="af7a6-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="af7a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af7a6-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSettings -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af7a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af7a6-105">DESCRIPTION</span></span>
<span data-ttu-id="af7a6-106">Командлет **Get-AzSqlServerAdvancedThreatProtectionSettings** получает расширенные параметры защиты от угроз для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="af7a6-106">The **Get-AzSqlServerAdvancedThreatProtectionSettings** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="af7a6-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера, для которого этот командлет получает параметры.</span><span class="sxs-lookup"><span data-stu-id="af7a6-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="af7a6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af7a6-108">EXAMPLES</span></span>

### <span data-ttu-id="af7a6-109">Пример 1: получение расширенных параметров защиты от угроз для сервера</span><span class="sxs-lookup"><span data-stu-id="af7a6-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="af7a6-110">Эта команда получает дополнительные параметры защиты от угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="af7a6-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="af7a6-111">Сервер назначается группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="af7a6-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="af7a6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af7a6-112">PARAMETERS</span></span>

### <span data-ttu-id="af7a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7a6-113">-DefaultProfile</span></span>
<span data-ttu-id="af7a6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="af7a6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af7a6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7a6-115">-ResourceGroupName</span></span>
<span data-ttu-id="af7a6-116">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="af7a6-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="af7a6-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="af7a6-117">-ServerName</span></span>
<span data-ttu-id="af7a6-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="af7a6-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="af7a6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af7a6-119">-Confirm</span></span>
<span data-ttu-id="af7a6-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af7a6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af7a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af7a6-121">-WhatIf</span></span>
<span data-ttu-id="af7a6-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af7a6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af7a6-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af7a6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af7a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7a6-124">CommonParameters</span></span>
<span data-ttu-id="af7a6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af7a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7a6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7a6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7a6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af7a6-127">INPUTS</span></span>

### <span data-ttu-id="af7a6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="af7a6-128">System.String</span></span>

## <span data-ttu-id="af7a6-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af7a6-129">OUTPUTS</span></span>

### <span data-ttu-id="af7a6-130">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="af7a6-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="af7a6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="af7a6-131">NOTES</span></span>

## <span data-ttu-id="af7a6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af7a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="af7a6-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="af7a6-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSettings.md)

[<span data-ttu-id="af7a6-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="af7a6-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


