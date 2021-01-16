---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415199"
---
# <span data-ttu-id="86c19-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="86c19-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="86c19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c19-102">SYNOPSIS</span></span>
<span data-ttu-id="86c19-103">Создает объект сведений об организации для сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="86c19-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="86c19-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86c19-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c19-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c19-105">DESCRIPTION</span></span>
<span data-ttu-id="86c19-106">**Новый-AzKeyVaultCertificateOrganizationDetail** создает в памяти объект сведений о организации сертификата.</span><span class="sxs-lookup"><span data-stu-id="86c19-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="86c19-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86c19-107">EXAMPLES</span></span>

### <span data-ttu-id="86c19-108">Пример 1. Создание объекта сведений об организации</span><span class="sxs-lookup"><span data-stu-id="86c19-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="86c19-109">Первая команда создает объект сведений администратора сертификата, а затем сохраняет его в $AdminDetails переменной.</span><span class="sxs-lookup"><span data-stu-id="86c19-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="86c19-110">Вторая команда создает объект сведений о организации сертификата, а затем сохраняет его в $OrgDetails переменной.</span><span class="sxs-lookup"><span data-stu-id="86c19-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="86c19-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86c19-111">PARAMETERS</span></span>

### <span data-ttu-id="86c19-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="86c19-112">-AdministratorDetails</span></span>
<span data-ttu-id="86c19-113">Указывает администраторов организации с сертификатами.</span><span class="sxs-lookup"><span data-stu-id="86c19-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="86c19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c19-114">-DefaultProfile</span></span>
<span data-ttu-id="86c19-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86c19-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86c19-116">-Id</span><span class="sxs-lookup"><span data-stu-id="86c19-116">-Id</span></span>
<span data-ttu-id="86c19-117">Определяет идентификатор для организации.</span><span class="sxs-lookup"><span data-stu-id="86c19-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="86c19-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86c19-118">-Confirm</span></span>
<span data-ttu-id="86c19-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c19-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c19-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c19-120">-WhatIf</span></span>
<span data-ttu-id="86c19-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c19-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c19-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="86c19-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c19-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c19-123">CommonParameters</span></span>
<span data-ttu-id="86c19-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c19-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c19-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86c19-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c19-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86c19-126">INPUTS</span></span>

### <span data-ttu-id="86c19-127">System.String</span><span class="sxs-lookup"><span data-stu-id="86c19-127">System.String</span></span>

### <span data-ttu-id="86c19-128">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="86c19-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="86c19-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86c19-129">OUTPUTS</span></span>

### <span data-ttu-id="86c19-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="86c19-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="86c19-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86c19-131">NOTES</span></span>

## <span data-ttu-id="86c19-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86c19-132">RELATED LINKS</span></span>

[<span data-ttu-id="86c19-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="86c19-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)
