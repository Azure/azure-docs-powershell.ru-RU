---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 18117a109448ec219364ee6563191683a1fbc8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563860"
---
# <span data-ttu-id="546f6-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="546f6-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="546f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="546f6-102">SYNOPSIS</span></span>
<span data-ttu-id="546f6-103">Получает параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="546f6-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="546f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="546f6-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="546f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="546f6-105">DESCRIPTION</span></span>
<span data-ttu-id="546f6-106">Командлет **Get-AzureRmSqlServerAuditing** получает политику аудита больших двоичных объектов для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="546f6-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="546f6-107">Укажите параметры *ResourceGroupName* и *ServerName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="546f6-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="546f6-108">Этот командлет возвращает политику, которая используется базами данных Azure SQL, определенными в указанном сервере Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="546f6-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="546f6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="546f6-109">EXAMPLES</span></span>

### <span data-ttu-id="546f6-110">Пример 1: получение параметров аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="546f6-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="546f6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="546f6-111">PARAMETERS</span></span>

### <span data-ttu-id="546f6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546f6-112">-ResourceGroupName</span></span>
<span data-ttu-id="546f6-113">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="546f6-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="546f6-114">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="546f6-114">-ServerName</span></span>
<span data-ttu-id="546f6-115">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="546f6-115">SQL server name.</span></span>

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

### <span data-ttu-id="546f6-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="546f6-116">-Confirm</span></span>
<span data-ttu-id="546f6-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="546f6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="546f6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="546f6-118">-WhatIf</span></span>
<span data-ttu-id="546f6-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="546f6-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="546f6-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="546f6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="546f6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546f6-121">-DefaultProfile</span></span>
<span data-ttu-id="546f6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="546f6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="546f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546f6-123">CommonParameters</span></span>
<span data-ttu-id="546f6-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="546f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546f6-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546f6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546f6-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="546f6-126">INPUTS</span></span>

## <span data-ttu-id="546f6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="546f6-127">OUTPUTS</span></span>

### <span data-ttu-id="546f6-128">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="546f6-128">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="546f6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="546f6-129">NOTES</span></span>

## <span data-ttu-id="546f6-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="546f6-130">RELATED LINKS</span></span>

