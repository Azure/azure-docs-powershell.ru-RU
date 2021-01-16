---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419668"
---
# <span data-ttu-id="35ce9-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="35ce9-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="35ce9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="35ce9-103">Добавляет прозрачный сертификат шифрования данных для управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="35ce9-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="35ce9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35ce9-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ce9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ce9-105">DESCRIPTION</span></span>
<span data-ttu-id="35ce9-106">В Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate добавляется прозрачный сертификат шифрования данных для управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="35ce9-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="35ce9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35ce9-107">EXAMPLES</span></span>

### <span data-ttu-id="35ce9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35ce9-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="35ce9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35ce9-109">PARAMETERS</span></span>

### <span data-ttu-id="35ce9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ce9-110">-DefaultProfile</span></span>
<span data-ttu-id="35ce9-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35ce9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35ce9-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="35ce9-112">-ManagedInstanceName</span></span>
<span data-ttu-id="35ce9-113">Имя управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="35ce9-113">The managed instance name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ce9-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35ce9-114">-PassThru</span></span>
<span data-ttu-id="35ce9-115">При успешном выполнении возвращает добавленный объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="35ce9-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="35ce9-116">-Password</span><span class="sxs-lookup"><span data-stu-id="35ce9-116">-Password</span></span>
<span data-ttu-id="35ce9-117">Пароль для прозрачного сертификата шифрования данных</span><span class="sxs-lookup"><span data-stu-id="35ce9-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ce9-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="35ce9-118">-PrivateBlob</span></span>
<span data-ttu-id="35ce9-119">Частный BLOB-проект для прозрачного сертификата шифрования данных</span><span class="sxs-lookup"><span data-stu-id="35ce9-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="35ce9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ce9-120">-ResourceGroupName</span></span>
<span data-ttu-id="35ce9-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="35ce9-121">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ce9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35ce9-122">-Confirm</span></span>
<span data-ttu-id="35ce9-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ce9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ce9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ce9-124">-WhatIf</span></span>
<span data-ttu-id="35ce9-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35ce9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ce9-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35ce9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ce9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ce9-127">CommonParameters</span></span>
<span data-ttu-id="35ce9-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ce9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ce9-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35ce9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ce9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35ce9-130">INPUTS</span></span>

### <span data-ttu-id="35ce9-131">Нет</span><span class="sxs-lookup"><span data-stu-id="35ce9-131">None</span></span>

## <span data-ttu-id="35ce9-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35ce9-132">OUTPUTS</span></span>

### <span data-ttu-id="35ce9-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35ce9-133">System.Boolean</span></span>

## <span data-ttu-id="35ce9-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35ce9-134">NOTES</span></span>

## <span data-ttu-id="35ce9-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35ce9-135">RELATED LINKS</span></span>
