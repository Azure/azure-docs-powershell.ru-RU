---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
ms.openlocfilehash: 76e0d37ac38c8b9799093ff3a4f4ea10c2fce2f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914457"
---
# <span data-ttu-id="36bf8-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="36bf8-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="36bf8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="36bf8-103">Создает объект подробных сведений об организации сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="36bf8-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36bf8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36bf8-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36bf8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="36bf8-106">Командлет **New-AzureKeyVaultCertificateOrganizationDetails** создает объект подробных сведений об организации сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="36bf8-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="36bf8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="36bf8-108">Пример 1: создание объекта сведений об Организации</span><span class="sxs-lookup"><span data-stu-id="36bf8-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="36bf8-109">В первой команде создается объект сведений администратора сертификата, который затем сохраняется в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="36bf8-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="36bf8-110">Вторая команда создает объект сведений об организации сертификата и сохраняет его в переменной $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="36bf8-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="36bf8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36bf8-111">PARAMETERS</span></span>

### <span data-ttu-id="36bf8-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="36bf8-112">-AdministratorDetails</span></span>
<span data-ttu-id="36bf8-113">Указывает администраторов организации сертификата.</span><span class="sxs-lookup"><span data-stu-id="36bf8-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="36bf8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bf8-114">-DefaultProfile</span></span>
<span data-ttu-id="36bf8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36bf8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36bf8-116">-ID</span><span class="sxs-lookup"><span data-stu-id="36bf8-116">-Id</span></span>
<span data-ttu-id="36bf8-117">Указывает идентификатор организации.</span><span class="sxs-lookup"><span data-stu-id="36bf8-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="36bf8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36bf8-118">-Confirm</span></span>
<span data-ttu-id="36bf8-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36bf8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36bf8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36bf8-120">-WhatIf</span></span>
<span data-ttu-id="36bf8-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36bf8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36bf8-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36bf8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36bf8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bf8-123">CommonParameters</span></span>
<span data-ttu-id="36bf8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36bf8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bf8-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36bf8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bf8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36bf8-126">INPUTS</span></span>

## <span data-ttu-id="36bf8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36bf8-127">OUTPUTS</span></span>

### <span data-ttu-id="36bf8-128">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="36bf8-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="36bf8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="36bf8-129">NOTES</span></span>

## <span data-ttu-id="36bf8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36bf8-130">RELATED LINKS</span></span>

[<span data-ttu-id="36bf8-131">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="36bf8-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

