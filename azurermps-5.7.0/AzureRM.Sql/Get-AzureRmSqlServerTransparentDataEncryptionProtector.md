---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: ecb49271c49e441140a43f8cb8ae5d65be56cd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733952"
---
# <span data-ttu-id="11db1-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="11db1-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="11db1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11db1-102">SYNOPSIS</span></span>
<span data-ttu-id="11db1-103">Получает предохранитель прозрачного шифрования данных (TDE).</span><span class="sxs-lookup"><span data-stu-id="11db1-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11db1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11db1-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11db1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11db1-105">DESCRIPTION</span></span>
<span data-ttu-id="11db1-106">Командлет Get-AzureRmSqlServerTransparentDataEncryptionProtector получает сведения о предохранителе TDE.</span><span class="sxs-lookup"><span data-stu-id="11db1-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="11db1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11db1-107">EXAMPLES</span></span>

### <span data-ttu-id="11db1-108">Пример 1: получение предохранителя прозрачного шифрования данных (TDE)</span><span class="sxs-lookup"><span data-stu-id="11db1-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="11db1-109">Эта команда получает предохранитель TDE для сервера с именем ContosoServer в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="11db1-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="11db1-110">ResourceGroupName ИмяСервера Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="11db1-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="11db1-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="11db1-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="11db1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11db1-112">PARAMETERS</span></span>

### <span data-ttu-id="11db1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11db1-113">-DefaultProfile</span></span>
<span data-ttu-id="11db1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="11db1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11db1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11db1-115">-ResourceGroupName</span></span>
<span data-ttu-id="11db1-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11db1-116">The name of the resource group</span></span>

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

### <span data-ttu-id="11db1-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="11db1-117">-ServerName</span></span>
<span data-ttu-id="11db1-118">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="11db1-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="11db1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11db1-119">-Confirm</span></span>
<span data-ttu-id="11db1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11db1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11db1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11db1-121">-WhatIf</span></span>
<span data-ttu-id="11db1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11db1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11db1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11db1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11db1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11db1-124">CommonParameters</span></span>
<span data-ttu-id="11db1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11db1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11db1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11db1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11db1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11db1-127">INPUTS</span></span>

### <span data-ttu-id="11db1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="11db1-128">System.String</span></span>

## <span data-ttu-id="11db1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11db1-129">OUTPUTS</span></span>

### <span data-ttu-id="11db1-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="11db1-130">System.Object</span></span>

## <span data-ttu-id="11db1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="11db1-131">NOTES</span></span>

## <span data-ttu-id="11db1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11db1-132">RELATED LINKS</span></span>

[<span data-ttu-id="11db1-133">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="11db1-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
