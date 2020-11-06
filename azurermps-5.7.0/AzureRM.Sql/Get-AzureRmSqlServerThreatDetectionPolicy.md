---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5ee1039f938c561424ded9768e9d5f84372410fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557055"
---
# <span data-ttu-id="27bdb-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="27bdb-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="27bdb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="27bdb-103">Возвращает политику обнаружения угроз для сервера.</span><span class="sxs-lookup"><span data-stu-id="27bdb-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27bdb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27bdb-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27bdb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27bdb-105">DESCRIPTION</span></span>
<span data-ttu-id="27bdb-106">Командлет **Get-AzureRmSqlServerThreatDetectionPolicy** получает политику обнаружения угроз для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="27bdb-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="27bdb-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера, для которого этот командлет получает политику.</span><span class="sxs-lookup"><span data-stu-id="27bdb-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="27bdb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27bdb-108">EXAMPLES</span></span>

### <span data-ttu-id="27bdb-109">Пример 1: получение политики обнаружения угроз для сервера</span><span class="sxs-lookup"><span data-stu-id="27bdb-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="27bdb-110">Эта команда получает политику обнаружения угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="27bdb-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="27bdb-111">Сервер назначается группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="27bdb-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="27bdb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27bdb-112">PARAMETERS</span></span>

### <span data-ttu-id="27bdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27bdb-113">-DefaultProfile</span></span>
<span data-ttu-id="27bdb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="27bdb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27bdb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27bdb-115">-ResourceGroupName</span></span>
<span data-ttu-id="27bdb-116">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="27bdb-116">Specifies the name of the resource group to which the server belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bdb-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="27bdb-117">-ServerName</span></span>
<span data-ttu-id="27bdb-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="27bdb-118">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27bdb-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27bdb-119">-Confirm</span></span>
<span data-ttu-id="27bdb-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27bdb-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27bdb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27bdb-121">-WhatIf</span></span>
<span data-ttu-id="27bdb-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27bdb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27bdb-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27bdb-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27bdb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27bdb-124">CommonParameters</span></span>
<span data-ttu-id="27bdb-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27bdb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27bdb-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27bdb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27bdb-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27bdb-127">INPUTS</span></span>

### <span data-ttu-id="27bdb-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="27bdb-128">None</span></span>
<span data-ttu-id="27bdb-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="27bdb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27bdb-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27bdb-130">OUTPUTS</span></span>

### <span data-ttu-id="27bdb-131">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="27bdb-131">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="27bdb-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="27bdb-132">NOTES</span></span>

## <span data-ttu-id="27bdb-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27bdb-133">RELATED LINKS</span></span>

[<span data-ttu-id="27bdb-134">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="27bdb-134">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="27bdb-135">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="27bdb-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


