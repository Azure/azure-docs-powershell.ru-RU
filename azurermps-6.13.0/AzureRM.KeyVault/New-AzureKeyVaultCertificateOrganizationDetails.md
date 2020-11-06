---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 7ce93670f6974e51fe634dea3adf81d3800b3a1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567746"
---
# <span data-ttu-id="a8092-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="a8092-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="a8092-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8092-102">SYNOPSIS</span></span>
<span data-ttu-id="a8092-103">Создает объект подробных сведений об организации сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="a8092-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8092-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8092-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8092-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8092-105">DESCRIPTION</span></span>
<span data-ttu-id="a8092-106">Командлет **New-AzureKeyVaultCertificateOrganizationDetails** создает объект подробных сведений об организации сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="a8092-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="a8092-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8092-107">EXAMPLES</span></span>

### <span data-ttu-id="a8092-108">Пример 1: создание объекта сведений об Организации</span><span class="sxs-lookup"><span data-stu-id="a8092-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzureKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="a8092-109">В первой команде создается объект сведений администратора сертификата, который затем сохраняется в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="a8092-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="a8092-110">Вторая команда создает объект сведений об организации сертификата и сохраняет его в переменной $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="a8092-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="a8092-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8092-111">PARAMETERS</span></span>

### <span data-ttu-id="a8092-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="a8092-112">-AdministratorDetails</span></span>
<span data-ttu-id="a8092-113">Указывает администраторов организации сертификата.</span><span class="sxs-lookup"><span data-stu-id="a8092-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8092-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8092-114">-DefaultProfile</span></span>
<span data-ttu-id="a8092-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8092-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8092-116">-ID</span><span class="sxs-lookup"><span data-stu-id="a8092-116">-Id</span></span>
<span data-ttu-id="a8092-117">Указывает идентификатор организации.</span><span class="sxs-lookup"><span data-stu-id="a8092-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="a8092-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8092-118">-Confirm</span></span>
<span data-ttu-id="a8092-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8092-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8092-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8092-120">-WhatIf</span></span>
<span data-ttu-id="a8092-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8092-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8092-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8092-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8092-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8092-123">CommonParameters</span></span>
<span data-ttu-id="a8092-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8092-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8092-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8092-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8092-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8092-126">INPUTS</span></span>

### <span data-ttu-id="a8092-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a8092-127">System.String</span></span>

### <span data-ttu-id="a8092-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateAdministratorDetails, Microsoft. Azure. Commands. KeyVault, Version = 5.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="a8092-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.Commands.KeyVault, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a8092-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8092-129">OUTPUTS</span></span>

### <span data-ttu-id="a8092-130">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="a8092-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="a8092-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8092-131">NOTES</span></span>

## <span data-ttu-id="a8092-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8092-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8092-133">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="a8092-133">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

