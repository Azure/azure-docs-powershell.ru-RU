---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlServerTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerTransparentDataEncryptionCertificate.md
ms.openlocfilehash: beb51449ea0264defe640ba60ad687be405ab669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961448"
---
# <span data-ttu-id="cb13e-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="cb13e-101">Add-AzSqlServerTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="cb13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb13e-102">SYNOPSIS</span></span>
<span data-ttu-id="cb13e-103">Добавляет прозрачный сертификат шифрования данных для экземпляра SQL Server данных.</span><span class="sxs-lookup"><span data-stu-id="cb13e-103">Adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="cb13e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb13e-104">SYNTAX</span></span>

### <span data-ttu-id="cb13e-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb13e-105">AddAzureRmSqlServerTransparentDataEncryptionCertificateDefaultParameterSet (Default)</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ServerName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb13e-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb13e-106">AddAzureRmSqlServerTransparentDataEncryptionCertificateInputObjectParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServer] <AzureSqlServerModel>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb13e-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb13e-107">AddAzureRmSqlServerTransparentDataEncryptionCertificateResourceIdParameterSet</span></span>
```
Add-AzSqlServerTransparentDataEncryptionCertificate [-PassThru] [-SqlServerResourceId] <String>
 [-PrivateBlob] <SecureString> [-Password] <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb13e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb13e-108">DESCRIPTION</span></span>
<span data-ttu-id="cb13e-109">В Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate добавляется прозрачный сертификат шифрования данных для SQL Server экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cb13e-109">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given SQL Server instance</span></span>

## <span data-ttu-id="cb13e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb13e-110">EXAMPLES</span></span>

### <span data-ttu-id="cb13e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb13e-111">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ServerName "YourServerName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="cb13e-112">Добавление сертификата TDE на SQL-сервер с использованием имени группы ресурсов и имени SQL Server ресурса</span><span class="sxs-lookup"><span data-stu-id="cb13e-112">Add TDE certificate to a sql server using resource group name and SQL Server name</span></span>

### <span data-ttu-id="cb13e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cb13e-113">Example 2</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $server = Get-AzSqlServer -ServerName "YourServerName" -ResourceGroupName "YourResourceGroupName" 
PS C:\>     Add-AzSqlServerTransparentDataEncryptionCertificate -SqlServerResourceId $server.ResourceId -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="cb13e-114">Добавление сертификата TDE на серверы с помощью ид ресурса сервера</span><span class="sxs-lookup"><span data-stu-id="cb13e-114">Add TDE certificate to the servers using server resourceId</span></span>

### <span data-ttu-id="cb13e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cb13e-115">Example 3</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
Get-AzSqlServer | Add-AzSqlServerTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

<span data-ttu-id="cb13e-116">Добавление сертификата TDE на все SQL-серверы в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="cb13e-116">Add TDE certificate to all sql servers in a resource group</span></span>

## <span data-ttu-id="cb13e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb13e-117">PARAMETERS</span></span>

### <span data-ttu-id="cb13e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb13e-118">-DefaultProfile</span></span>
<span data-ttu-id="cb13e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb13e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb13e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb13e-120">-PassThru</span></span>
<span data-ttu-id="cb13e-121">При успешном выполнении возвращает добавленный объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb13e-121">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="cb13e-122">-Password</span><span class="sxs-lookup"><span data-stu-id="cb13e-122">-Password</span></span>
<span data-ttu-id="cb13e-123">Пароль для прозрачного сертификата шифрования данных</span><span class="sxs-lookup"><span data-stu-id="cb13e-123">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="cb13e-124">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="cb13e-124">-PrivateBlob</span></span>
<span data-ttu-id="cb13e-125">Частный BLOB-проект для прозрачного сертификата шифрования данных</span><span class="sxs-lookup"><span data-stu-id="cb13e-125">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="cb13e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb13e-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb13e-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cb13e-127">The Resource Group Name</span></span>

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

### <span data-ttu-id="cb13e-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb13e-128">-ServerName</span></span>
<span data-ttu-id="cb13e-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="cb13e-129">The Server Name</span></span>

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

### <span data-ttu-id="cb13e-130">-SqlServer</span><span class="sxs-lookup"><span data-stu-id="cb13e-130">-SqlServer</span></span>
<span data-ttu-id="cb13e-131">Объект ввода SQL Server</span><span class="sxs-lookup"><span data-stu-id="cb13e-131">The sql server input object</span></span>

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

### <span data-ttu-id="cb13e-132">-SqlServerResourceId</span><span class="sxs-lookup"><span data-stu-id="cb13e-132">-SqlServerResourceId</span></span>
<span data-ttu-id="cb13e-133">The sql server resource id</span><span class="sxs-lookup"><span data-stu-id="cb13e-133">The sql server resource id</span></span>

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

### <span data-ttu-id="cb13e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb13e-134">-Confirm</span></span>
<span data-ttu-id="cb13e-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb13e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb13e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb13e-136">-WhatIf</span></span>
<span data-ttu-id="cb13e-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb13e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb13e-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cb13e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb13e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb13e-139">CommonParameters</span></span>
<span data-ttu-id="cb13e-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb13e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb13e-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb13e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb13e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb13e-142">INPUTS</span></span>

### <span data-ttu-id="cb13e-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="cb13e-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="cb13e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cb13e-144">System.String</span></span>

## <span data-ttu-id="cb13e-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb13e-145">OUTPUTS</span></span>

### <span data-ttu-id="cb13e-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb13e-146">System.Boolean</span></span>

## <span data-ttu-id="cb13e-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb13e-147">NOTES</span></span>

## <span data-ttu-id="cb13e-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb13e-148">RELATED LINKS</span></span>
