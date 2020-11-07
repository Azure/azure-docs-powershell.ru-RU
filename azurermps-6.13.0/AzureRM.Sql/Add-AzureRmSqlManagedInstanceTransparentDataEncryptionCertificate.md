---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 9fe8e36a752b4643ba44a59e8c44954bf25284c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732578"
---
# <span data-ttu-id="fe03b-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="fe03b-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="fe03b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe03b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe03b-103">Добавляет прозрачный сертификат шифрования данных для заданного управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fe03b-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe03b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe03b-104">SYNTAX</span></span>

```
Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe03b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe03b-105">DESCRIPTION</span></span>
<span data-ttu-id="fe03b-106">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate добавляет прозрачный сертификат шифрования данных для данного управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fe03b-106">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="fe03b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe03b-107">EXAMPLES</span></span>

### <span data-ttu-id="fe03b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe03b-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="fe03b-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe03b-109">PARAMETERS</span></span>

### <span data-ttu-id="fe03b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe03b-110">-DefaultProfile</span></span>
<span data-ttu-id="fe03b-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe03b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe03b-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="fe03b-112">-ManagedInstanceName</span></span>
<span data-ttu-id="fe03b-113">Имя управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="fe03b-113">The managed instance name</span></span>

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

### <span data-ttu-id="fe03b-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe03b-114">-PassThru</span></span>
<span data-ttu-id="fe03b-115">При успешном выполнении возвращает объект сертификата, который был добавлен.</span><span class="sxs-lookup"><span data-stu-id="fe03b-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="fe03b-116">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="fe03b-116">-Password</span></span>
<span data-ttu-id="fe03b-117">Пароль для сертификата шифрования прозрачных данных</span><span class="sxs-lookup"><span data-stu-id="fe03b-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="fe03b-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="fe03b-118">-PrivateBlob</span></span>
<span data-ttu-id="fe03b-119">Закрытый большой двоичный объект для прозрачного сертификата шифрования данных</span><span class="sxs-lookup"><span data-stu-id="fe03b-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="fe03b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe03b-120">-ResourceGroupName</span></span>
<span data-ttu-id="fe03b-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fe03b-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="fe03b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe03b-122">-Confirm</span></span>
<span data-ttu-id="fe03b-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe03b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe03b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe03b-124">-WhatIf</span></span>
<span data-ttu-id="fe03b-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe03b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe03b-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe03b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe03b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe03b-127">CommonParameters</span></span>
<span data-ttu-id="fe03b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe03b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe03b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe03b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe03b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe03b-130">INPUTS</span></span>

### <span data-ttu-id="fe03b-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="fe03b-131">None</span></span>

## <span data-ttu-id="fe03b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe03b-132">OUTPUTS</span></span>

### <span data-ttu-id="fe03b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe03b-133">System.Boolean</span></span>

## <span data-ttu-id="fe03b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe03b-134">NOTES</span></span>

## <span data-ttu-id="fe03b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe03b-135">RELATED LINKS</span></span>
