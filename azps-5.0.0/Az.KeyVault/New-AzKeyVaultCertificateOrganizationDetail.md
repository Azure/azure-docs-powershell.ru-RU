---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250213"
---
# <span data-ttu-id="800c4-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="800c4-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="800c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="800c4-102">SYNOPSIS</span></span>
<span data-ttu-id="800c4-103">Создает объект подробных сведений об организации сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="800c4-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="800c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="800c4-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="800c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="800c4-105">DESCRIPTION</span></span>
<span data-ttu-id="800c4-106">Командлет **New-AzKeyVaultCertificateOrganizationDetail** создает объект подробных сведений об организации сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="800c4-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="800c4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="800c4-107">EXAMPLES</span></span>

### <span data-ttu-id="800c4-108">Пример 1: создание объекта сведений об Организации</span><span class="sxs-lookup"><span data-stu-id="800c4-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="800c4-109">В первой команде создается объект сведений администратора сертификата, который затем сохраняется в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="800c4-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="800c4-110">Вторая команда создает объект сведений об организации сертификата и сохраняет его в переменной $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="800c4-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="800c4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="800c4-111">PARAMETERS</span></span>

### <span data-ttu-id="800c4-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="800c4-112">-AdministratorDetails</span></span>
<span data-ttu-id="800c4-113">Указывает администраторов организации сертификата.</span><span class="sxs-lookup"><span data-stu-id="800c4-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="800c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800c4-114">-DefaultProfile</span></span>
<span data-ttu-id="800c4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="800c4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="800c4-116">-ID</span><span class="sxs-lookup"><span data-stu-id="800c4-116">-Id</span></span>
<span data-ttu-id="800c4-117">Указывает идентификатор организации.</span><span class="sxs-lookup"><span data-stu-id="800c4-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="800c4-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="800c4-118">-Confirm</span></span>
<span data-ttu-id="800c4-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="800c4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="800c4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800c4-120">-WhatIf</span></span>
<span data-ttu-id="800c4-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="800c4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="800c4-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="800c4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="800c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800c4-123">CommonParameters</span></span>
<span data-ttu-id="800c4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="800c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800c4-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="800c4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800c4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="800c4-126">INPUTS</span></span>

### <span data-ttu-id="800c4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="800c4-127">System.String</span></span>

### <span data-ttu-id="800c4-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateAdministratorDetails, Microsoft. Azure. PowerShell. командлеты. KeyVault, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="800c4-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="800c4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="800c4-129">OUTPUTS</span></span>

### <span data-ttu-id="800c4-130">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="800c4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="800c4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="800c4-131">NOTES</span></span>

## <span data-ttu-id="800c4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="800c4-132">RELATED LINKS</span></span>

[<span data-ttu-id="800c4-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="800c4-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

