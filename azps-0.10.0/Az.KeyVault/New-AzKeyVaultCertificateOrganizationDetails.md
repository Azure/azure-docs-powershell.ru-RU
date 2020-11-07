---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911169"
---
# <span data-ttu-id="7a1fd-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="7a1fd-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="7a1fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1fd-103">Создает объект подробных сведений об организации сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="7a1fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a1fd-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a1fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a1fd-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1fd-106">Командлет **New-AzKeyVaultCertificateOrganizationDetails** создает объект подробных сведений об организации сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="7a1fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a1fd-107">EXAMPLES</span></span>

### <span data-ttu-id="7a1fd-108">Пример 1: создание объекта сведений об Организации</span><span class="sxs-lookup"><span data-stu-id="7a1fd-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="7a1fd-109">В первой команде создается объект сведений администратора сертификата, который затем сохраняется в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="7a1fd-110">Вторая команда создает объект сведений об организации сертификата и сохраняет его в переменной $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="7a1fd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a1fd-111">PARAMETERS</span></span>

### <span data-ttu-id="7a1fd-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="7a1fd-112">-AdministratorDetails</span></span>
<span data-ttu-id="7a1fd-113">Указывает администраторов организации сертификата.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1fd-114">-DefaultProfile</span></span>
<span data-ttu-id="7a1fd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7a1fd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a1fd-116">-ID</span><span class="sxs-lookup"><span data-stu-id="7a1fd-116">-Id</span></span>
<span data-ttu-id="7a1fd-117">Указывает идентификатор организации.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="7a1fd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a1fd-118">-Confirm</span></span>
<span data-ttu-id="7a1fd-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a1fd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a1fd-120">-WhatIf</span></span>
<span data-ttu-id="7a1fd-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a1fd-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a1fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1fd-123">CommonParameters</span></span>
<span data-ttu-id="7a1fd-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1fd-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a1fd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1fd-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a1fd-126">INPUTS</span></span>

### <span data-ttu-id="7a1fd-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="7a1fd-127">None</span></span>
<span data-ttu-id="7a1fd-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a1fd-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a1fd-129">OUTPUTS</span></span>

### <span data-ttu-id="7a1fd-130">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="7a1fd-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="7a1fd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a1fd-131">NOTES</span></span>

## <span data-ttu-id="7a1fd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a1fd-132">RELATED LINKS</span></span>

[<span data-ttu-id="7a1fd-133">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="7a1fd-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

