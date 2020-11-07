---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 6cb14b368bf7f190c30ff32fdec12576d3189204
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729011"
---
# <span data-ttu-id="d237e-101">Get-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d237e-101">Get-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="d237e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d237e-102">SYNOPSIS</span></span>
<span data-ttu-id="d237e-103">Возвращает политику обнаружения угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="d237e-103">Gets the threat detection policy for a database.</span></span>

## <span data-ttu-id="d237e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d237e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d237e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d237e-105">DESCRIPTION</span></span>
<span data-ttu-id="d237e-106">Командлет **Get-AzSqlDatabaseThreatDetectionPolicy** получает политику обнаружения угроз для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d237e-106">The **Get-AzSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="d237e-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы определить базу данных, для которой этот командлет получает политику.</span><span class="sxs-lookup"><span data-stu-id="d237e-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="d237e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d237e-108">EXAMPLES</span></span>

### <span data-ttu-id="d237e-109">Пример 1: получение политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="d237e-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="d237e-110">Эта команда получает политику обнаружения угроз для базы данных с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="d237e-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="d237e-111">База данных находится на сервере с именем Server01, который назначен группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d237e-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d237e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d237e-112">PARAMETERS</span></span>

### <span data-ttu-id="d237e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d237e-113">-DatabaseName</span></span>
<span data-ttu-id="d237e-114">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d237e-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="d237e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d237e-115">-DefaultProfile</span></span>
<span data-ttu-id="d237e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d237e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d237e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d237e-117">-ResourceGroupName</span></span>
<span data-ttu-id="d237e-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="d237e-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d237e-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d237e-119">-ServerName</span></span>
<span data-ttu-id="d237e-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d237e-120">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="d237e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d237e-121">-Confirm</span></span>
<span data-ttu-id="d237e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d237e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d237e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d237e-123">-WhatIf</span></span>
<span data-ttu-id="d237e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d237e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d237e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d237e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d237e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d237e-126">CommonParameters</span></span>
<span data-ttu-id="d237e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d237e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d237e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d237e-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d237e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d237e-129">INPUTS</span></span>

### <span data-ttu-id="d237e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d237e-130">System.String</span></span>

## <span data-ttu-id="d237e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d237e-131">OUTPUTS</span></span>

### <span data-ttu-id="d237e-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d237e-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="d237e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d237e-133">NOTES</span></span>

## <span data-ttu-id="d237e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d237e-134">RELATED LINKS</span></span>

[<span data-ttu-id="d237e-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d237e-135">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)



