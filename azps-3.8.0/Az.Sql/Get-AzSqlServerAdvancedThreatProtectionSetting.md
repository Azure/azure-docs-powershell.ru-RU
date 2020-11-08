---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065255"
---
# <span data-ttu-id="6b304-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="6b304-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="6b304-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b304-102">SYNOPSIS</span></span>
<span data-ttu-id="6b304-103">Получает параметры расширенной защиты от угроз для сервера.</span><span class="sxs-lookup"><span data-stu-id="6b304-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="6b304-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b304-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b304-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b304-105">DESCRIPTION</span></span>
<span data-ttu-id="6b304-106">Командлет **Get-AzSqlServerAdvancedThreatProtectionSetting** получает расширенные параметры защиты от угроз для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6b304-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="6b304-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера, для которого этот командлет получает параметры.</span><span class="sxs-lookup"><span data-stu-id="6b304-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="6b304-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b304-108">EXAMPLES</span></span>

### <span data-ttu-id="6b304-109">Пример 1: получение расширенных параметров защиты от угроз для сервера</span><span class="sxs-lookup"><span data-stu-id="6b304-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="6b304-110">Эта команда получает дополнительные параметры защиты от угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="6b304-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="6b304-111">Сервер назначается группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6b304-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="6b304-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b304-112">PARAMETERS</span></span>

### <span data-ttu-id="6b304-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b304-113">-DefaultProfile</span></span>
<span data-ttu-id="6b304-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b304-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b304-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b304-115">-ResourceGroupName</span></span>
<span data-ttu-id="6b304-116">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="6b304-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="6b304-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6b304-117">-ServerName</span></span>
<span data-ttu-id="6b304-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6b304-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6b304-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b304-119">-Confirm</span></span>
<span data-ttu-id="6b304-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b304-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b304-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b304-121">-WhatIf</span></span>
<span data-ttu-id="6b304-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b304-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b304-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b304-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b304-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b304-124">CommonParameters</span></span>
<span data-ttu-id="6b304-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b304-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b304-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b304-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b304-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b304-127">INPUTS</span></span>

### <span data-ttu-id="6b304-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6b304-128">System.String</span></span>

## <span data-ttu-id="6b304-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b304-129">OUTPUTS</span></span>

### <span data-ttu-id="6b304-130">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="6b304-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="6b304-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b304-131">NOTES</span></span>

## <span data-ttu-id="6b304-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b304-132">RELATED LINKS</span></span>

[<span data-ttu-id="6b304-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="6b304-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="6b304-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="6b304-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


