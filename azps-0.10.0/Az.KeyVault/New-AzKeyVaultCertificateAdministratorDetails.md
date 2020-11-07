---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 6844a8f4858452a1ebf9df306d75e495603703aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910292"
---
# <span data-ttu-id="564e7-101">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="564e7-101">New-AzKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="564e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="564e7-102">SYNOPSIS</span></span>
<span data-ttu-id="564e7-103">Создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="564e7-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="564e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="564e7-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="564e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="564e7-105">DESCRIPTION</span></span>
<span data-ttu-id="564e7-106">Командлет **New-AzKeyVaultCertificateAdministratorDetails** создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="564e7-106">The **New-AzKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="564e7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="564e7-107">EXAMPLES</span></span>

### <span data-ttu-id="564e7-108">Пример 1: создание объекта сведений для администратора сертификата</span><span class="sxs-lookup"><span data-stu-id="564e7-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="564e7-109">Эта команда создает объект сведений администратора сертификата в памяти и сохраняет его в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="564e7-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="564e7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="564e7-110">PARAMETERS</span></span>

### <span data-ttu-id="564e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564e7-111">-DefaultProfile</span></span>
<span data-ttu-id="564e7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="564e7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="564e7-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="564e7-113">-EmailAddress</span></span>
<span data-ttu-id="564e7-114">Указывает адрес электронной почты для администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="564e7-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="564e7-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="564e7-115">-FirstName</span></span>
<span data-ttu-id="564e7-116">Задает имя администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="564e7-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="564e7-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="564e7-117">-LastName</span></span>
<span data-ttu-id="564e7-118">Задает фамилию администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="564e7-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="564e7-119">-Заданный</span><span class="sxs-lookup"><span data-stu-id="564e7-119">-PhoneNumber</span></span>
<span data-ttu-id="564e7-120">Задает номер телефона администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="564e7-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="564e7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="564e7-121">-Confirm</span></span>
<span data-ttu-id="564e7-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="564e7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="564e7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="564e7-123">-WhatIf</span></span>
<span data-ttu-id="564e7-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="564e7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="564e7-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="564e7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="564e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564e7-126">CommonParameters</span></span>
<span data-ttu-id="564e7-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="564e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564e7-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="564e7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564e7-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="564e7-129">INPUTS</span></span>

### <span data-ttu-id="564e7-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="564e7-130">None</span></span>
<span data-ttu-id="564e7-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="564e7-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="564e7-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="564e7-132">OUTPUTS</span></span>

### <span data-ttu-id="564e7-133">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="564e7-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="564e7-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="564e7-134">NOTES</span></span>

## <span data-ttu-id="564e7-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="564e7-135">RELATED LINKS</span></span>

[<span data-ttu-id="564e7-136">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="564e7-136">New-AzKeyVaultCertificateOrganizationDetails</span></span>](./New-AzKeyVaultCertificateOrganizationDetails.md)

