---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: f8d01165825c63ece34779f58cb94a3f8e0af40c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728932"
---
# <span data-ttu-id="00329-101">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="00329-101">Get-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="00329-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00329-102">SYNOPSIS</span></span>
<span data-ttu-id="00329-103">Возвращает политику обнаружения угроз для сервера.</span><span class="sxs-lookup"><span data-stu-id="00329-103">Gets the threat detection policy for a server.</span></span>

## <span data-ttu-id="00329-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00329-104">SYNTAX</span></span>

```
Get-AzSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00329-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00329-105">DESCRIPTION</span></span>
<span data-ttu-id="00329-106">Командлет **Get-AzSqlServerThreatDetectionPolicy** получает политику обнаружения угроз для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="00329-106">The **Get-AzSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="00329-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера, для которого этот командлет получает политику.</span><span class="sxs-lookup"><span data-stu-id="00329-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="00329-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00329-108">EXAMPLES</span></span>

### <span data-ttu-id="00329-109">Пример 1: получение политики обнаружения угроз для сервера</span><span class="sxs-lookup"><span data-stu-id="00329-109">Example 1: Get the threat detection policy for a server</span></span>
```
PS C:\>Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="00329-110">Эта команда получает политику обнаружения угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="00329-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="00329-111">Сервер назначается группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="00329-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="00329-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00329-112">PARAMETERS</span></span>

### <span data-ttu-id="00329-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00329-113">-DefaultProfile</span></span>
<span data-ttu-id="00329-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="00329-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00329-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00329-115">-ResourceGroupName</span></span>
<span data-ttu-id="00329-116">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="00329-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="00329-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="00329-117">-ServerName</span></span>
<span data-ttu-id="00329-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="00329-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="00329-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00329-119">-Confirm</span></span>
<span data-ttu-id="00329-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00329-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00329-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00329-121">-WhatIf</span></span>
<span data-ttu-id="00329-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00329-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00329-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00329-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00329-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00329-124">CommonParameters</span></span>
<span data-ttu-id="00329-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00329-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00329-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00329-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00329-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00329-127">INPUTS</span></span>

### <span data-ttu-id="00329-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00329-128">System.String</span></span>

## <span data-ttu-id="00329-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00329-129">OUTPUTS</span></span>

### <span data-ttu-id="00329-130">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="00329-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="00329-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="00329-131">NOTES</span></span>

## <span data-ttu-id="00329-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00329-132">RELATED LINKS</span></span>

[<span data-ttu-id="00329-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="00329-133">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="00329-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="00329-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


