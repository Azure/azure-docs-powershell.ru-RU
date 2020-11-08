---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077580"
---
# <span data-ttu-id="bc82b-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="bc82b-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="bc82b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc82b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc82b-103">Добавляет прозрачный сертификат шифрования данных для заданного экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bc82b-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="bc82b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc82b-104">SYNTAX</span></span>

### <span data-ttu-id="bc82b-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc82b-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc82b-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc82b-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc82b-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc82b-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc82b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc82b-108">DESCRIPTION</span></span>
<span data-ttu-id="bc82b-109">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate добавляет прозрачный сертификат шифрования данных для заданного экземпляра SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bc82b-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="bc82b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc82b-110">EXAMPLES</span></span>

### <span data-ttu-id="bc82b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc82b-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="bc82b-112">Добавление сертификата TDE на сервер SQL Server с помощью имени группы ресурсов и имени сервера SQL Server</span><span class="sxs-lookup"><span data-stu-id="bc82b-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="bc82b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bc82b-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="bc82b-114">Добавление сертификата TDE на серверы с помощью сервера resourceId</span><span class="sxs-lookup"><span data-stu-id="bc82b-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="bc82b-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bc82b-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="bc82b-116">Добавление сертификата TDE на все серверы SQL в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="bc82b-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="bc82b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc82b-117">PARAMETERS</span></span>

### <span data-ttu-id="bc82b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc82b-118">-DefaultProfile</span></span>
<span data-ttu-id="bc82b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc82b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc82b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc82b-120">-PassThru</span></span>
<span data-ttu-id="bc82b-121">При успешном выполнении возвращает объект сертификата, который был добавлен.</span><span class="sxs-lookup"><span data-stu-id="bc82b-121">On Successful execution, returns certificate object that was added.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc82b-122">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="bc82b-122">-Password</span></span>
<span data-ttu-id="bc82b-123">Пароль для сертификата шифрования прозрачных данных</span><span class="sxs-lookup"><span data-stu-id="bc82b-123">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc82b-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="bc82b-124">-PrivateBlob</span></span>
<span data-ttu-id="bc82b-125">Закрытый большой двоичный объект для прозрачного сертификата шифрования данных</span><span class="sxs-lookup"><span data-stu-id="bc82b-125">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc82b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc82b-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc82b-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bc82b-127">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc82b-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bc82b-128">-ServerName</span></span>
<span data-ttu-id="bc82b-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="bc82b-129">The Server Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc82b-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="bc82b-130">-SqlServer</span></span>
<span data-ttu-id="bc82b-131">Входной объект SQL Server</span><span class="sxs-lookup"><span data-stu-id="bc82b-131">The sql server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc82b-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="bc82b-132">-SqlServerResourceId</span></span>
<span data-ttu-id="bc82b-133">Идентификатор ресурса SQL Server</span><span class="sxs-lookup"><span data-stu-id="bc82b-133">The sql server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc82b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc82b-134">-Confirm</span></span>
<span data-ttu-id="bc82b-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc82b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc82b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc82b-136">-WhatIf</span></span>
<span data-ttu-id="bc82b-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc82b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc82b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc82b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc82b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc82b-139">CommonParameters</span></span>
<span data-ttu-id="bc82b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc82b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc82b-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc82b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc82b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc82b-142">INPUTS</span></span>

### <span data-ttu-id="bc82b-143">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="bc82b-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="bc82b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="bc82b-144">System.String</span></span>

## <span data-ttu-id="bc82b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc82b-145">OUTPUTS</span></span>

### <span data-ttu-id="bc82b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc82b-146">System.Boolean</span></span>

## <span data-ttu-id="bc82b-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc82b-147">NOTES</span></span>

## <span data-ttu-id="bc82b-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc82b-148">RELATED LINKS</span></span>
