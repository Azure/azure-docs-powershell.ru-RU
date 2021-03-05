---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: e72729b1721fb31ca2ce3a52d33f0295c55bb537
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001368"
---
# <span data-ttu-id="26619-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="26619-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="26619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26619-102">SYNOPSIS</span></span>
<span data-ttu-id="26619-103">Создает объект сведений администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="26619-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="26619-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26619-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26619-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26619-105">DESCRIPTION</span></span>
<span data-ttu-id="26619-106">**Новый-AzKeyVaultCertificateAdministratorDetail** создает в памяти объект сведений администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="26619-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="26619-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26619-107">EXAMPLES</span></span>

### <span data-ttu-id="26619-108">Пример 1. Создание объекта сведений об администраторе сертификата</span><span class="sxs-lookup"><span data-stu-id="26619-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="26619-109">Эта команда создает объект сведений администратора сертификата в памяти и сохраняет его в переменной $AdminDetails памяти.</span><span class="sxs-lookup"><span data-stu-id="26619-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="26619-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26619-110">PARAMETERS</span></span>

### <span data-ttu-id="26619-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26619-111">-DefaultProfile</span></span>
<span data-ttu-id="26619-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="26619-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26619-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="26619-113">-EmailAddress</span></span>
<span data-ttu-id="26619-114">Адрес электронной почты администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="26619-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26619-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="26619-115">-FirstName</span></span>
<span data-ttu-id="26619-116">Указывает имя администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="26619-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26619-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="26619-117">-LastName</span></span>
<span data-ttu-id="26619-118">Указывает фамилию администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="26619-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26619-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="26619-119">-PhoneNumber</span></span>
<span data-ttu-id="26619-120">Номер телефона администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="26619-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26619-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26619-121">-Confirm</span></span>
<span data-ttu-id="26619-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26619-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26619-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26619-123">-WhatIf</span></span>
<span data-ttu-id="26619-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26619-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26619-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26619-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26619-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26619-126">CommonParameters</span></span>
<span data-ttu-id="26619-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26619-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26619-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26619-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26619-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26619-129">INPUTS</span></span>

### <span data-ttu-id="26619-130">System.String</span><span class="sxs-lookup"><span data-stu-id="26619-130">System.String</span></span>

## <span data-ttu-id="26619-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26619-131">OUTPUTS</span></span>

### <span data-ttu-id="26619-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="26619-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="26619-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26619-133">NOTES</span></span>

## <span data-ttu-id="26619-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26619-134">RELATED LINKS</span></span>

[<span data-ttu-id="26619-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="26619-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

