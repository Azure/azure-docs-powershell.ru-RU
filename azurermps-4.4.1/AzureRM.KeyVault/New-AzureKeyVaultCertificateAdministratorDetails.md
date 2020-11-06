---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 28a2bb0c806fa152a742c2fc9e36b150116a6352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559771"
---
# <span data-ttu-id="e1822-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="e1822-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="e1822-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1822-102">SYNOPSIS</span></span>
<span data-ttu-id="e1822-103">Создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="e1822-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1822-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1822-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1822-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1822-105">DESCRIPTION</span></span>
<span data-ttu-id="e1822-106">Командлет **New-AzureKeyVaultCertificateAdministratorDetails** создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="e1822-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="e1822-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1822-107">EXAMPLES</span></span>

### <span data-ttu-id="e1822-108">Пример 1: создание объекта сведений для администратора сертификата</span><span class="sxs-lookup"><span data-stu-id="e1822-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="e1822-109">Эта команда создает объект сведений администратора сертификата в памяти и сохраняет его в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="e1822-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="e1822-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1822-110">PARAMETERS</span></span>

### <span data-ttu-id="e1822-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e1822-111">-EmailAddress</span></span>
<span data-ttu-id="e1822-112">Указывает адрес электронной почты для администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="e1822-112">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="e1822-113">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e1822-113">-FirstName</span></span>
<span data-ttu-id="e1822-114">Задает имя администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="e1822-114">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="e1822-115">-LastName</span><span class="sxs-lookup"><span data-stu-id="e1822-115">-LastName</span></span>
<span data-ttu-id="e1822-116">Задает фамилию администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="e1822-116">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="e1822-117">-Заданный</span><span class="sxs-lookup"><span data-stu-id="e1822-117">-PhoneNumber</span></span>
<span data-ttu-id="e1822-118">Задает номер телефона администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="e1822-118">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="e1822-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1822-119">-Confirm</span></span>
<span data-ttu-id="e1822-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1822-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1822-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1822-121">-WhatIf</span></span>
<span data-ttu-id="e1822-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1822-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1822-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1822-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1822-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1822-124">-DefaultProfile</span></span>
<span data-ttu-id="e1822-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1822-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1822-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1822-126">CommonParameters</span></span>
<span data-ttu-id="e1822-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1822-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1822-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1822-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1822-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1822-129">INPUTS</span></span>

## <span data-ttu-id="e1822-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1822-130">OUTPUTS</span></span>

### <span data-ttu-id="e1822-131">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="e1822-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="e1822-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1822-132">NOTES</span></span>

## <span data-ttu-id="e1822-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1822-133">RELATED LINKS</span></span>

[<span data-ttu-id="e1822-134">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="e1822-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

