---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 017EF522-ABC5-40EE-B8DC-369D097F49D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: ed1e01b5d49aaf31404f1db4d55fd31a253faca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560428"
---
# <span data-ttu-id="2c370-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c370-101">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="2c370-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c370-102">SYNOPSIS</span></span>
<span data-ttu-id="2c370-103">Возвращает политику обнаружения угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2c370-103">Gets the threat detection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c370-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c370-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseThreatDetectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c370-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c370-105">DESCRIPTION</span></span>
<span data-ttu-id="2c370-106">Командлет **Get-AzureRmSqlDatabaseThreatDetectionPolicy** получает политику обнаружения угроз для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2c370-106">The **Get-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL database.</span></span>
<span data-ttu-id="2c370-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы определить базу данных, для которой этот командлет получает политику.</span><span class="sxs-lookup"><span data-stu-id="2c370-107">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="2c370-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c370-108">EXAMPLES</span></span>

### <span data-ttu-id="2c370-109">Пример 1: получение политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="2c370-109">Example 1: Get the threat detection policy for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="2c370-110">Эта команда получает политику обнаружения угроз для базы данных с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="2c370-110">This command gets the threat detection policy for a database named Database01.</span></span>
<span data-ttu-id="2c370-111">База данных находится на сервере с именем Server01, который назначен группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2c370-111">The database is located on the server named Server01, which is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="2c370-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c370-112">PARAMETERS</span></span>

### <span data-ttu-id="2c370-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c370-113">-DatabaseName</span></span>
<span data-ttu-id="2c370-114">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2c370-114">Specifies the name of a database.</span></span>

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

### <span data-ttu-id="2c370-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c370-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c370-116">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="2c370-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2c370-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2c370-117">-ServerName</span></span>
<span data-ttu-id="2c370-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2c370-118">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="2c370-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c370-119">-Confirm</span></span>
<span data-ttu-id="2c370-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c370-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c370-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c370-121">-WhatIf</span></span>
<span data-ttu-id="2c370-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c370-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c370-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c370-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c370-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c370-124">-DefaultProfile</span></span>
<span data-ttu-id="2c370-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c370-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c370-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c370-126">CommonParameters</span></span>
<span data-ttu-id="2c370-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c370-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c370-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c370-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c370-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c370-129">INPUTS</span></span>

###  
<span data-ttu-id="2c370-130">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2c370-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="2c370-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c370-131">OUTPUTS</span></span>

### <span data-ttu-id="2c370-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2c370-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="2c370-133">Этот командлет возвращает объект **model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="2c370-133">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="2c370-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c370-134">NOTES</span></span>

## <span data-ttu-id="2c370-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c370-135">RELATED LINKS</span></span>

[<span data-ttu-id="2c370-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c370-136">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)



