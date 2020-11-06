---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 1cb77a435ee951e2e7fe4bc7401e7e4385557eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567496"
---
# <span data-ttu-id="f194d-101">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f194d-101">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="f194d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f194d-102">SYNOPSIS</span></span>
<span data-ttu-id="f194d-103">Возвращает политику обнаружения угроз для сервера.</span><span class="sxs-lookup"><span data-stu-id="f194d-103">Gets the threat detection policy for a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f194d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f194d-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerThreatDetectionPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f194d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f194d-105">DESCRIPTION</span></span>
<span data-ttu-id="f194d-106">Командлет **Get-AzureRmSqlServerThreatDetectionPolicy** получает политику обнаружения угроз для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f194d-106">The **Get-AzureRmSqlServerThreatDetectionPolicy** cmdlet gets the threat detection policy of an Azure SQL server.</span></span>
<span data-ttu-id="f194d-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера, для которого этот командлет получает политику.</span><span class="sxs-lookup"><span data-stu-id="f194d-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the policy.</span></span>

## <span data-ttu-id="f194d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f194d-108">EXAMPLES</span></span>

### <span data-ttu-id="f194d-109">Пример 1: получение политики обнаружения угроз для сервера</span><span class="sxs-lookup"><span data-stu-id="f194d-109">Example 1: Get the threat detection policy for a server</span></span>
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

<span data-ttu-id="f194d-110">Эта команда получает политику обнаружения угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="f194d-110">This command gets the threat detection policy for a server named Server01.</span></span>
<span data-ttu-id="f194d-111">Сервер назначается группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f194d-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="f194d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f194d-112">PARAMETERS</span></span>

### <span data-ttu-id="f194d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f194d-113">-ResourceGroupName</span></span>
<span data-ttu-id="f194d-114">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="f194d-114">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="f194d-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f194d-115">-ServerName</span></span>
<span data-ttu-id="f194d-116">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f194d-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f194d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f194d-117">-Confirm</span></span>
<span data-ttu-id="f194d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f194d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f194d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f194d-119">-WhatIf</span></span>
<span data-ttu-id="f194d-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f194d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f194d-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f194d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f194d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f194d-122">-DefaultProfile</span></span>
<span data-ttu-id="f194d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f194d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f194d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f194d-124">CommonParameters</span></span>
<span data-ttu-id="f194d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f194d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f194d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f194d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f194d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f194d-127">INPUTS</span></span>

## <span data-ttu-id="f194d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f194d-128">OUTPUTS</span></span>

### <span data-ttu-id="f194d-129">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f194d-129">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="f194d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f194d-130">NOTES</span></span>

## <span data-ttu-id="f194d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f194d-131">RELATED LINKS</span></span>

[<span data-ttu-id="f194d-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f194d-132">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="f194d-133">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f194d-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


