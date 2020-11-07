---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: fb64d30618eb736434c34ae1d47059433b336779
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900189"
---
# <span data-ttu-id="f96b1-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="f96b1-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="f96b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f96b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f96b1-103">Создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="f96b1-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="f96b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f96b1-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f96b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f96b1-105">DESCRIPTION</span></span>
<span data-ttu-id="f96b1-106">Командлет **New-AzKeyVaultCertificateAdministratorDetail** создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="f96b1-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="f96b1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f96b1-107">EXAMPLES</span></span>

### <span data-ttu-id="f96b1-108">Пример 1: создание объекта сведений для администратора сертификата</span><span class="sxs-lookup"><span data-stu-id="f96b1-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="f96b1-109">Эта команда создает объект сведений администратора сертификата в памяти и сохраняет его в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="f96b1-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="f96b1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f96b1-110">PARAMETERS</span></span>

### <span data-ttu-id="f96b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f96b1-111">-DefaultProfile</span></span>
<span data-ttu-id="f96b1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f96b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f96b1-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f96b1-113">-EmailAddress</span></span>
<span data-ttu-id="f96b1-114">Указывает адрес электронной почты для администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="f96b1-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="f96b1-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="f96b1-115">-FirstName</span></span>
<span data-ttu-id="f96b1-116">Задает имя администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="f96b1-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="f96b1-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="f96b1-117">-LastName</span></span>
<span data-ttu-id="f96b1-118">Задает фамилию администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="f96b1-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="f96b1-119">-Заданный</span><span class="sxs-lookup"><span data-stu-id="f96b1-119">-PhoneNumber</span></span>
<span data-ttu-id="f96b1-120">Задает номер телефона администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="f96b1-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="f96b1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f96b1-121">-Confirm</span></span>
<span data-ttu-id="f96b1-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f96b1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f96b1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f96b1-123">-WhatIf</span></span>
<span data-ttu-id="f96b1-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f96b1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f96b1-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f96b1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f96b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f96b1-126">CommonParameters</span></span>
<span data-ttu-id="f96b1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f96b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f96b1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f96b1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f96b1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f96b1-129">INPUTS</span></span>

### <span data-ttu-id="f96b1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f96b1-130">System.String</span></span>

## <span data-ttu-id="f96b1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f96b1-131">OUTPUTS</span></span>

### <span data-ttu-id="f96b1-132">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="f96b1-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="f96b1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f96b1-133">NOTES</span></span>

## <span data-ttu-id="f96b1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f96b1-134">RELATED LINKS</span></span>

[<span data-ttu-id="f96b1-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="f96b1-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

