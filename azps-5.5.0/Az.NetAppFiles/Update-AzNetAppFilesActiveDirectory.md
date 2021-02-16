---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237161"
---
# <span data-ttu-id="36d8c-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="36d8c-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="36d8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="36d8c-103">Обновляет конфигурацию active directory Azure NetApp Files (ANF) до предоставленных необязательных модификаторов.</span><span class="sxs-lookup"><span data-stu-id="36d8c-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="36d8c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36d8c-104">SYNTAX</span></span>

### <span data-ttu-id="36d8c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36d8c-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d8c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36d8c-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d8c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36d8c-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36d8c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d8c-108">DESCRIPTION</span></span>
<span data-ttu-id="36d8c-109">Для **настройки active directory ANF будет модифицируется cmdlet Update-AzNetAppFilesAccount.**</span><span class="sxs-lookup"><span data-stu-id="36d8c-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="36d8c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36d8c-110">EXAMPLES</span></span>

### <span data-ttu-id="36d8c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36d8c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="36d8c-112">Эта команда обновляет заданную конфигурацию active directory, внося изменения в имя пользователя в этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="36d8c-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="36d8c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36d8c-113">PARAMETERS</span></span>

### <span data-ttu-id="36d8c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36d8c-114">-AccountName</span></span>
<span data-ttu-id="36d8c-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="36d8c-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="36d8c-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="36d8c-116">-AccountObject</span></span>
<span data-ttu-id="36d8c-117">Учетная запись объекта Active Directory</span><span class="sxs-lookup"><span data-stu-id="36d8c-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="36d8c-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="36d8c-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="36d8c-119">ИД активного каталога ANF</span><span class="sxs-lookup"><span data-stu-id="36d8c-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d8c-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="36d8c-120">-AdName</span></span>
<span data-ttu-id="36d8c-121">Имя компьютера Active Directory.</span><span class="sxs-lookup"><span data-stu-id="36d8c-121">Name of the active directory machine.</span></span>
<span data-ttu-id="36d8c-122">Этот необязательный параметр используется только при создании громкости kerberos.</span><span class="sxs-lookup"><span data-stu-id="36d8c-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="36d8c-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="36d8c-123">-BackupOperator</span></span>
<span data-ttu-id="36d8c-124">Пользователи, которые будут добавлены в группу active directory "Встроенный оператор резервного копирования".</span><span class="sxs-lookup"><span data-stu-id="36d8c-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="36d8c-125">Список уникальных имен пользователей без замера домена</span><span class="sxs-lookup"><span data-stu-id="36d8c-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="36d8c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d8c-126">-DefaultProfile</span></span>
<span data-ttu-id="36d8c-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36d8c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d8c-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="36d8c-128">-Dns</span></span>
<span data-ttu-id="36d8c-129">Разделенный запятой список IP-адресов DNS-сервера (только IPv4) для домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="36d8c-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="36d8c-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="36d8c-130">-Domain</span></span>
<span data-ttu-id="36d8c-131">Имя домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="36d8c-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="36d8c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36d8c-132">-InputObject</span></span>
<span data-ttu-id="36d8c-133">Объект Active Directory, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="36d8c-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36d8c-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="36d8c-134">-KdcIP</span></span>
<span data-ttu-id="36d8c-135">IP-адреса сервера KDC для компьютера Active Directory.</span><span class="sxs-lookup"><span data-stu-id="36d8c-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="36d8c-136">Этот необязательный параметр используется только при создании громкости kerberos.</span><span class="sxs-lookup"><span data-stu-id="36d8c-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="36d8c-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="36d8c-137">-OrganizationalUnit</span></span>
<span data-ttu-id="36d8c-138">Подразделение в Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="36d8c-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="36d8c-139">-Password</span><span class="sxs-lookup"><span data-stu-id="36d8c-139">-Password</span></span>
<span data-ttu-id="36d8c-140">Обычный текстовый пароль администратора домена Active Directory, значение маск находится в ответе</span><span class="sxs-lookup"><span data-stu-id="36d8c-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="36d8c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d8c-141">-ResourceGroupName</span></span>
<span data-ttu-id="36d8c-142">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="36d8c-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="36d8c-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="36d8c-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="36d8c-144">Если служба LDAP включена через протокол SSL/TLS, клиенту LDAP необходим самозаверязательный корневой сертификат ЦС службы Active Directory с кодированием базовой кодировки, этот необязательный параметр используется только для двух протоколов с томами сопоставления пользователей LDAP.</span><span class="sxs-lookup"><span data-stu-id="36d8c-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="36d8c-145">-Site</span><span class="sxs-lookup"><span data-stu-id="36d8c-145">-Site</span></span>
<span data-ttu-id="36d8c-146">На сайте Active Directory служба ограничивает обнаружение контроллеров доменов только</span><span class="sxs-lookup"><span data-stu-id="36d8c-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="36d8c-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="36d8c-147">-SmbServerName</span></span>
<span data-ttu-id="36d8c-148">NetBIOS имя сервера SMB.</span><span class="sxs-lookup"><span data-stu-id="36d8c-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="36d8c-149">Это имя будет зарегистрировано как учетная запись компьютера в AD и использоваться для установки громкости</span><span class="sxs-lookup"><span data-stu-id="36d8c-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="36d8c-150">-Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="36d8c-150">-Username</span></span>
<span data-ttu-id="36d8c-151">Имя пользователя администратора домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="36d8c-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="36d8c-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36d8c-152">-Confirm</span></span>
<span data-ttu-id="36d8c-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="36d8c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d8c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d8c-154">-WhatIf</span></span>
<span data-ttu-id="36d8c-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36d8c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d8c-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36d8c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d8c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d8c-157">CommonParameters</span></span>
<span data-ttu-id="36d8c-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d8c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d8c-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36d8c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d8c-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36d8c-160">INPUTS</span></span>

### <span data-ttu-id="36d8c-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="36d8c-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="36d8c-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="36d8c-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="36d8c-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36d8c-163">OUTPUTS</span></span>

### <span data-ttu-id="36d8c-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="36d8c-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="36d8c-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36d8c-165">NOTES</span></span>

## <span data-ttu-id="36d8c-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36d8c-166">RELATED LINKS</span></span>
