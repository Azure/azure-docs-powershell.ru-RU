---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 636b3602c6dafc2c00e02e19aa35d0e91c278137
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561439"
---
# <span data-ttu-id="61b32-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="61b32-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="61b32-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61b32-102">SYNOPSIS</span></span>
<span data-ttu-id="61b32-103">Получает параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61b32-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61b32-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61b32-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61b32-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61b32-105">DESCRIPTION</span></span>
<span data-ttu-id="61b32-106">Командлет **Get-AzureRmSqlServerAuditing** получает политику аудита больших двоичных объектов для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61b32-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="61b32-107">Укажите параметры *ResourceGroupName* и *ServerName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="61b32-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="61b32-108">Этот командлет возвращает политику, которая используется базами данных Azure SQL, определенными в указанном сервере Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61b32-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="61b32-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61b32-109">EXAMPLES</span></span>

### <span data-ttu-id="61b32-110">Пример 1: получение параметров аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="61b32-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="61b32-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61b32-111">PARAMETERS</span></span>

### <span data-ttu-id="61b32-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b32-112">-DefaultProfile</span></span>
<span data-ttu-id="61b32-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61b32-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61b32-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61b32-114">-ResourceGroupName</span></span>
<span data-ttu-id="61b32-115">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61b32-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="61b32-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="61b32-116">-ServerName</span></span>
<span data-ttu-id="61b32-117">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="61b32-117">SQL server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61b32-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61b32-118">-Confirm</span></span>
<span data-ttu-id="61b32-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61b32-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b32-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61b32-120">-WhatIf</span></span>
<span data-ttu-id="61b32-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61b32-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61b32-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61b32-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b32-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b32-123">CommonParameters</span></span>
<span data-ttu-id="61b32-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61b32-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b32-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b32-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b32-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61b32-126">INPUTS</span></span>

### <span data-ttu-id="61b32-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="61b32-127">None</span></span>
<span data-ttu-id="61b32-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="61b32-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61b32-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61b32-129">OUTPUTS</span></span>

### <span data-ttu-id="61b32-130">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="61b32-130">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="61b32-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="61b32-131">NOTES</span></span>

## <span data-ttu-id="61b32-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61b32-132">RELATED LINKS</span></span>
