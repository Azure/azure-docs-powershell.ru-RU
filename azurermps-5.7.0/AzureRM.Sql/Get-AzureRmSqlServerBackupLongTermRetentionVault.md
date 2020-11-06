---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 567cb47599a23bf83581afb97a425902ee0e159a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561432"
---
# <span data-ttu-id="4c898-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="4c898-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="4c898-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c898-102">SYNOPSIS</span></span>
<span data-ttu-id="4c898-103">Возвращает серверное хранилище долгосрочного хранения.</span><span class="sxs-lookup"><span data-stu-id="4c898-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c898-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c898-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c898-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c898-105">DESCRIPTION</span></span>
<span data-ttu-id="4c898-106">Командлет **Get-AzureRmSqlServerBackupLongTermRetentionVault** получает долгосрочное хранилище, которое зарегистрировано для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="4c898-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="4c898-107">Хранилище — это ресурс резервного копирования Azure, который используется для хранения данных резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="4c898-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="4c898-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c898-108">EXAMPLES</span></span>

## <span data-ttu-id="4c898-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c898-109">PARAMETERS</span></span>

### <span data-ttu-id="4c898-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c898-110">-DefaultProfile</span></span>
<span data-ttu-id="4c898-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4c898-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c898-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c898-112">-ResourceGroupName</span></span>
<span data-ttu-id="4c898-113">Указывает имя группы ресурсов, содержащей сервер.</span><span class="sxs-lookup"><span data-stu-id="4c898-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="4c898-114">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4c898-114">-ServerName</span></span>
<span data-ttu-id="4c898-115">Указывает сервер, для которого этот командлет получает хранилище.</span><span class="sxs-lookup"><span data-stu-id="4c898-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="4c898-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c898-116">-Confirm</span></span>
<span data-ttu-id="4c898-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c898-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c898-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c898-118">-WhatIf</span></span>
<span data-ttu-id="4c898-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c898-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c898-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c898-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c898-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c898-121">CommonParameters</span></span>
<span data-ttu-id="4c898-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c898-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c898-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c898-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c898-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c898-124">INPUTS</span></span>

### <span data-ttu-id="4c898-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="4c898-125">None</span></span>
<span data-ttu-id="4c898-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4c898-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c898-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c898-127">OUTPUTS</span></span>

## <span data-ttu-id="4c898-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c898-128">NOTES</span></span>

## <span data-ttu-id="4c898-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c898-129">RELATED LINKS</span></span>

[<span data-ttu-id="4c898-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="4c898-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="4c898-131">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="4c898-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

