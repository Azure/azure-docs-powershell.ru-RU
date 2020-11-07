---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 663ac3d8342e5ba231276e560408f8f7f6e74741
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735038"
---
# <span data-ttu-id="2f062-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="2f062-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="2f062-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f062-102">SYNOPSIS</span></span>
<span data-ttu-id="2f062-103">Задает долговременное хранилище сервера в течение длительного срока хранения.</span><span class="sxs-lookup"><span data-stu-id="2f062-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f062-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f062-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f062-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f062-105">DESCRIPTION</span></span>
<span data-ttu-id="2f062-106">Командлет **Set-AzureRmSqlServerBackupLongTermRetentionVault** задает долгосрочный банк хранения, зарегистрированный для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="2f062-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="2f062-107">Хранилище — это ресурс резервного копирования Azure, который используется для хранения данных резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="2f062-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="2f062-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f062-108">EXAMPLES</span></span>

## <span data-ttu-id="2f062-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f062-109">PARAMETERS</span></span>

### <span data-ttu-id="2f062-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f062-110">-ResourceGroupName</span></span>
<span data-ttu-id="2f062-111">Указывает имя группы ресурсов, содержащей сервер.</span><span class="sxs-lookup"><span data-stu-id="2f062-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="2f062-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f062-112">-ResourceId</span></span>
<span data-ttu-id="2f062-113">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2f062-113">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f062-114">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2f062-114">-ServerName</span></span>
<span data-ttu-id="2f062-115">Указывает сервер, для которого этот командлет задает хранилище.</span><span class="sxs-lookup"><span data-stu-id="2f062-115">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="2f062-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f062-116">-Confirm</span></span>
<span data-ttu-id="2f062-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f062-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f062-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f062-118">-WhatIf</span></span>
<span data-ttu-id="2f062-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f062-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f062-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f062-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f062-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f062-121">-DefaultProfile</span></span>
<span data-ttu-id="2f062-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f062-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f062-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f062-123">CommonParameters</span></span>
<span data-ttu-id="2f062-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f062-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f062-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f062-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f062-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f062-126">INPUTS</span></span>

## <span data-ttu-id="2f062-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f062-127">OUTPUTS</span></span>

## <span data-ttu-id="2f062-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f062-128">NOTES</span></span>

## <span data-ttu-id="2f062-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f062-129">RELATED LINKS</span></span>

[<span data-ttu-id="2f062-130">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="2f062-130">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="2f062-131">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2f062-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
