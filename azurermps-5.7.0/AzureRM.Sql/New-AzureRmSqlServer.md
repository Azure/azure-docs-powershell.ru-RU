---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServer.md
ms.openlocfilehash: 6b9fa4c7fff426f9af19484c7576b9dee341a82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732830"
---
# <span data-ttu-id="6bd28-101">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6bd28-101">New-AzureRmSqlServer</span></span>

## <span data-ttu-id="6bd28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6bd28-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd28-103">Создание сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="6bd28-103">Creates a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bd28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6bd28-104">SYNTAX</span></span>

```
New-AzureRmSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bd28-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bd28-105">DESCRIPTION</span></span>
<span data-ttu-id="6bd28-106">Командлет **New-AzureRmSqlServer** создает сервер базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6bd28-106">The **New-AzureRmSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="6bd28-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6bd28-107">EXAMPLES</span></span>

### <span data-ttu-id="6bd28-108">Пример 1: создание нового сервера базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="6bd28-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="6bd28-109">Эта команда создает сервер базы данных SQL Azure версии 12.</span><span class="sxs-lookup"><span data-stu-id="6bd28-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="6bd28-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6bd28-110">PARAMETERS</span></span>

### <span data-ttu-id="6bd28-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bd28-111">-AsJob</span></span>
<span data-ttu-id="6bd28-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6bd28-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd28-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6bd28-113">-AssignIdentity</span></span>
<span data-ttu-id="6bd28-114">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6bd28-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd28-115">-DefaultProfile</span></span>
<span data-ttu-id="6bd28-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6bd28-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bd28-117">-Location</span><span class="sxs-lookup"><span data-stu-id="6bd28-117">-Location</span></span>
<span data-ttu-id="6bd28-118">Указывает расположение центра обработки данных, в котором этот командлет создает сервер.</span><span class="sxs-lookup"><span data-stu-id="6bd28-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd28-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd28-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bd28-120">Указывает имя группы ресурсов, к которой этот командлет назначает сервер.</span><span class="sxs-lookup"><span data-stu-id="6bd28-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="6bd28-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6bd28-121">-ServerName</span></span>
<span data-ttu-id="6bd28-122">Указывает имя нового сервера.</span><span class="sxs-lookup"><span data-stu-id="6bd28-122">Specifies the name of the new server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd28-123">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="6bd28-123">-ServerVersion</span></span>
<span data-ttu-id="6bd28-124">Указывает версию нового сервера.</span><span class="sxs-lookup"><span data-stu-id="6bd28-124">Specifies the version of the new server.</span></span> <span data-ttu-id="6bd28-125">Допустимые значения этого параметра: 2,0 и 12,0.</span><span class="sxs-lookup"><span data-stu-id="6bd28-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

<span data-ttu-id="6bd28-126">Укажите 2,0 для создания сервера версии 11 или 12,0, чтобы создать сервер версии 12.</span><span class="sxs-lookup"><span data-stu-id="6bd28-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd28-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="6bd28-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="6bd28-128">Задает учетные данные администратора сервера базы данных SQL для нового сервера.</span><span class="sxs-lookup"><span data-stu-id="6bd28-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="6bd28-129">Чтобы получить объект **PSCredential** , используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="6bd28-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="6bd28-130">Для получения дополнительных сведений введите `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="6bd28-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd28-131">-Теги</span><span class="sxs-lookup"><span data-stu-id="6bd28-131">-Tags</span></span>
<span data-ttu-id="6bd28-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="6bd28-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6bd28-133">Например:</span><span class="sxs-lookup"><span data-stu-id="6bd28-133">For example:</span></span>

<span data-ttu-id="6bd28-134">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="6bd28-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bd28-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bd28-135">-Confirm</span></span>
<span data-ttu-id="6bd28-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6bd28-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd28-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd28-137">-WhatIf</span></span>
<span data-ttu-id="6bd28-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6bd28-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd28-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6bd28-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bd28-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd28-140">CommonParameters</span></span>
<span data-ttu-id="6bd28-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6bd28-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd28-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd28-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd28-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6bd28-143">INPUTS</span></span>

### <span data-ttu-id="6bd28-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="6bd28-144">None</span></span>
<span data-ttu-id="6bd28-145">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6bd28-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6bd28-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bd28-146">OUTPUTS</span></span>

### <span data-ttu-id="6bd28-147">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="6bd28-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="6bd28-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="6bd28-148">NOTES</span></span>

## <span data-ttu-id="6bd28-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bd28-149">RELATED LINKS</span></span>

[<span data-ttu-id="6bd28-150">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6bd28-150">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="6bd28-151">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6bd28-151">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="6bd28-152">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="6bd28-152">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="6bd28-153">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6bd28-153">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="6bd28-154">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="6bd28-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
