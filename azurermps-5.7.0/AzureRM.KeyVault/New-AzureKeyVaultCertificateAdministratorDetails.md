---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 01d0718e4efeae093b7bd9ed4fc2c6bca4cf7f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734997"
---
# <span data-ttu-id="61da6-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="61da6-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="61da6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61da6-102">SYNOPSIS</span></span>
<span data-ttu-id="61da6-103">Создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="61da6-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61da6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61da6-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61da6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61da6-105">DESCRIPTION</span></span>
<span data-ttu-id="61da6-106">Командлет **New-AzureKeyVaultCertificateAdministratorDetails** создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="61da6-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="61da6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61da6-107">EXAMPLES</span></span>

### <span data-ttu-id="61da6-108">Пример 1: создание объекта сведений для администратора сертификата</span><span class="sxs-lookup"><span data-stu-id="61da6-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="61da6-109">Эта команда создает объект сведений администратора сертификата в памяти и сохраняет его в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="61da6-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="61da6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61da6-110">PARAMETERS</span></span>

### <span data-ttu-id="61da6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61da6-111">-DefaultProfile</span></span>
<span data-ttu-id="61da6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61da6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61da6-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="61da6-113">-EmailAddress</span></span>
<span data-ttu-id="61da6-114">Указывает адрес электронной почты для администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="61da6-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61da6-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="61da6-115">-FirstName</span></span>
<span data-ttu-id="61da6-116">Задает имя администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="61da6-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61da6-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="61da6-117">-LastName</span></span>
<span data-ttu-id="61da6-118">Задает фамилию администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="61da6-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61da6-119">-Заданный</span><span class="sxs-lookup"><span data-stu-id="61da6-119">-PhoneNumber</span></span>
<span data-ttu-id="61da6-120">Задает номер телефона администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="61da6-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61da6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61da6-121">-Confirm</span></span>
<span data-ttu-id="61da6-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61da6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61da6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61da6-123">-WhatIf</span></span>
<span data-ttu-id="61da6-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61da6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61da6-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61da6-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61da6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61da6-126">CommonParameters</span></span>
<span data-ttu-id="61da6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61da6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61da6-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61da6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61da6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61da6-129">INPUTS</span></span>

### <span data-ttu-id="61da6-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="61da6-130">None</span></span>
<span data-ttu-id="61da6-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="61da6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61da6-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61da6-132">OUTPUTS</span></span>

### <span data-ttu-id="61da6-133">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="61da6-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="61da6-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="61da6-134">NOTES</span></span>

## <span data-ttu-id="61da6-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61da6-135">RELATED LINKS</span></span>

[<span data-ttu-id="61da6-136">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="61da6-136">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

