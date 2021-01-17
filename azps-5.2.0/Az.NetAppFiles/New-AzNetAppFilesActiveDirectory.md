---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410767"
---
# <span data-ttu-id="7a8f4-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="7a8f4-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="7a8f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a8f4-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8f4-103">Создает новую конфигурацию active directory Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="7a8f4-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="7a8f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a8f4-104">SYNTAX</span></span>

### <span data-ttu-id="7a8f4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a8f4-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a8f4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a8f4-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a8f4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a8f4-107">DESCRIPTION</span></span>
<span data-ttu-id="7a8f4-108">Для учетной записи ANF создается новая конфигурация Active Directory для **AzNetAppFilesActiveDirectory.**</span><span class="sxs-lookup"><span data-stu-id="7a8f4-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="7a8f4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a8f4-109">EXAMPLES</span></span>

### <span data-ttu-id="7a8f4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a8f4-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="7a8f4-111">Эта команда получает пароль AD из promt в новую конфигурацию Active Directory для учетной записи ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="7a8f4-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="7a8f4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a8f4-112">PARAMETERS</span></span>

### <span data-ttu-id="7a8f4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a8f4-113">-AccountName</span></span>
<span data-ttu-id="7a8f4-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="7a8f4-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="7a8f4-115">-AccountObject</span></span>
<span data-ttu-id="7a8f4-116">Учетная запись для нового объекта политики резервного копирования</span><span class="sxs-lookup"><span data-stu-id="7a8f4-116">The Account for the new Backup Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="7a8f4-117">-AdName</span></span>
<span data-ttu-id="7a8f4-118">Имя компьютера Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-118">Name of the active directory machine.</span></span>
<span data-ttu-id="7a8f4-119">Этот необязательный параметр используется только при создании громкости kerberos.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-119">This optional parameter is used only while creating kerberos volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="7a8f4-120">-BackupOperator</span></span>
<span data-ttu-id="7a8f4-121">Пользователей, которые будут добавлены в группу active directory "Встроенный оператор резервного копирования".</span><span class="sxs-lookup"><span data-stu-id="7a8f4-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="7a8f4-122">Список уникальных имен пользователей без замера домена</span><span class="sxs-lookup"><span data-stu-id="7a8f4-122">A list of unique usernames without domain specifier</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8f4-123">-DefaultProfile</span></span>
<span data-ttu-id="7a8f4-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a8f4-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="7a8f4-125">-Dns</span></span>
<span data-ttu-id="7a8f4-126">Разделенный запятой список IP-адресов DNS-сервера (только IPv4) для домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="7a8f4-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="7a8f4-127">-Domain</span></span>
<span data-ttu-id="7a8f4-128">Имя домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="7a8f4-128">Name of the Active Directory domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="7a8f4-129">-KdcIP</span></span>
<span data-ttu-id="7a8f4-130">IP-адреса сервера KDC для компьютера Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="7a8f4-131">Этот необязательный параметр используется только при создании громкости kerberos.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-131">This optional parameter is used only while creating kerberos volume.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="7a8f4-132">-OrganizationalUnit</span></span>
<span data-ttu-id="7a8f4-133">Подразделение в Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="7a8f4-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-134">-Password</span><span class="sxs-lookup"><span data-stu-id="7a8f4-134">-Password</span></span>
<span data-ttu-id="7a8f4-135">Обычный текстовый пароль администратора домена Active Directory, значение маск находится в ответе</span><span class="sxs-lookup"><span data-stu-id="7a8f4-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a8f4-136">-ResourceGroupName</span></span>
<span data-ttu-id="7a8f4-137">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="7a8f4-137">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="7a8f4-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="7a8f4-139">Если служба LDAP включена через протокол SSL/TLS, клиенту LDAP необходим самозаверязательный корневой сертификат ЦС службы Active Directory с кодированием базовой кодировки, этот необязательный параметр используется только для двух протоколов с томами сопоставления пользователей LDAP.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-140">-Site</span><span class="sxs-lookup"><span data-stu-id="7a8f4-140">-Site</span></span>
<span data-ttu-id="7a8f4-141">На сайте Active Directory служба ограничивает обнаружение контроллера домена только</span><span class="sxs-lookup"><span data-stu-id="7a8f4-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="7a8f4-142">-SmbServerName</span></span>
<span data-ttu-id="7a8f4-143">NetBIOS имя сервера SMB.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="7a8f4-144">Это имя будет зарегистрировано в качестве учетной записи компьютера в AD и используется для установки громкости</span><span class="sxs-lookup"><span data-stu-id="7a8f4-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-145">-Username</span><span class="sxs-lookup"><span data-stu-id="7a8f4-145">-Username</span></span>
<span data-ttu-id="7a8f4-146">Имя пользователя администратора домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="7a8f4-146">Username of Active Directory domain administrator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a8f4-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a8f4-147">-Confirm</span></span>
<span data-ttu-id="7a8f4-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a8f4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a8f4-149">-WhatIf</span></span>
<span data-ttu-id="7a8f4-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a8f4-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a8f4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8f4-152">CommonParameters</span></span>
<span data-ttu-id="7a8f4-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8f4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8f4-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a8f4-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8f4-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a8f4-155">INPUTS</span></span>

### <span data-ttu-id="7a8f4-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7a8f4-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7a8f4-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a8f4-157">OUTPUTS</span></span>

### <span data-ttu-id="7a8f4-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="7a8f4-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="7a8f4-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a8f4-159">NOTES</span></span>

## <span data-ttu-id="7a8f4-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a8f4-160">RELATED LINKS</span></span>
