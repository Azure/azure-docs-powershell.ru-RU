---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e90dac7c55c6edca849c483ccb21d4f37197883a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419660"
---
# <span data-ttu-id="cfd44-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="cfd44-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="cfd44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfd44-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd44-103">Добавляет прозрачный сертификат шифрования данных для экземпляра SQL Server данных.</span><span class="sxs-lookup"><span data-stu-id="cfd44-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="cfd44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cfd44-104">SYNTAX</span></span>

### <span data-ttu-id="cfd44-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cfd44-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfd44-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfd44-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfd44-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfd44-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd44-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfd44-108">DESCRIPTION</span></span>
<span data-ttu-id="cfd44-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span><span class="sxs-lookup"><span data-stu-id="cfd44-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="cfd44-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cfd44-110">EXAMPLES</span></span>

### <span data-ttu-id="cfd44-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfd44-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="cfd44-112">Добавление сертификата TDE на SQL-сервер с использованием имени группы ресурсов и имени SQL Server ресурса</span><span class="sxs-lookup"><span data-stu-id="cfd44-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="cfd44-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cfd44-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="cfd44-114">Добавление сертификата TDE на серверы с помощью ид ресурса сервера</span><span class="sxs-lookup"><span data-stu-id="cfd44-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="cfd44-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cfd44-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="cfd44-116">Добавление сертификата TDE во все SQL-серверы в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="cfd44-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="cfd44-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfd44-117">PARAMETERS</span></span>

### <span data-ttu-id="cfd44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd44-118">-DefaultProfile</span></span>
<span data-ttu-id="cfd44-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfd44-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfd44-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfd44-120">-PassThru</span></span>
<span data-ttu-id="cfd44-121">При успешном выполнении возвращает добавленный объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="cfd44-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="cfd44-122">-Password</span><span class="sxs-lookup"><span data-stu-id="cfd44-122">-Password</span></span>
<span data-ttu-id="cfd44-123">Пароль для прозрачного сертификата шифрования данных</span><span class="sxs-lookup"><span data-stu-id="cfd44-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="cfd44-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="cfd44-124">-PrivateBlob</span></span>
<span data-ttu-id="cfd44-125">Частный BLOB-проект для прозрачного сертификата шифрования данных</span><span class="sxs-lookup"><span data-stu-id="cfd44-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="cfd44-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd44-126">-ResourceGroupName</span></span>
<span data-ttu-id="cfd44-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cfd44-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="cfd44-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cfd44-128">-ServerName</span></span>
<span data-ttu-id="cfd44-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="cfd44-129">The Server Name</span></span>

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

### <span data-ttu-id="cfd44-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="cfd44-130">-SqlServer</span></span>
<span data-ttu-id="cfd44-131">Объект ввода SQL Server</span><span class="sxs-lookup"><span data-stu-id="cfd44-131">The sql server input object</span></span>

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

### <span data-ttu-id="cfd44-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd44-132">-SqlServerResourceId</span></span>
<span data-ttu-id="cfd44-133">The sql server resource id</span><span class="sxs-lookup"><span data-stu-id="cfd44-133">The sql server resource id</span></span>

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

### <span data-ttu-id="cfd44-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfd44-134">-Confirm</span></span>
<span data-ttu-id="cfd44-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfd44-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd44-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd44-136">-WhatIf</span></span>
<span data-ttu-id="cfd44-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfd44-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfd44-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cfd44-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfd44-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd44-139">CommonParameters</span></span>
<span data-ttu-id="cfd44-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfd44-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd44-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfd44-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd44-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfd44-142">INPUTS</span></span>

### <span data-ttu-id="cfd44-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="cfd44-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="cfd44-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cfd44-144">System.String</span></span>

## <span data-ttu-id="cfd44-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cfd44-145">OUTPUTS</span></span>

### <span data-ttu-id="cfd44-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cfd44-146">System.Boolean</span></span>

## <span data-ttu-id="cfd44-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cfd44-147">NOTES</span></span>

## <span data-ttu-id="cfd44-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfd44-148">RELATED LINKS</span></span>
