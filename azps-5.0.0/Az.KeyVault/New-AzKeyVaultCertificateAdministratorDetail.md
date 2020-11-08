---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248662"
---
# <span data-ttu-id="a5ac4-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="a5ac4-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="a5ac4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ac4-103">Создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="a5ac4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5ac4-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ac4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="a5ac4-106">Командлет **New-AzKeyVaultCertificateAdministratorDetail** создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="a5ac4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5ac4-107">EXAMPLES</span></span>

### <span data-ttu-id="a5ac4-108">Пример 1: создание объекта сведений для администратора сертификата</span><span class="sxs-lookup"><span data-stu-id="a5ac4-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="a5ac4-109">Эта команда создает объект сведений администратора сертификата в памяти и сохраняет его в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="a5ac4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5ac4-110">PARAMETERS</span></span>

### <span data-ttu-id="a5ac4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ac4-111">-DefaultProfile</span></span>
<span data-ttu-id="a5ac4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a5ac4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5ac4-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a5ac4-113">-EmailAddress</span></span>
<span data-ttu-id="a5ac4-114">Указывает адрес электронной почты для администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="a5ac4-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="a5ac4-115">-FirstName</span></span>
<span data-ttu-id="a5ac4-116">Задает имя администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="a5ac4-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="a5ac4-117">-LastName</span></span>
<span data-ttu-id="a5ac4-118">Задает фамилию администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="a5ac4-119">-Заданный</span><span class="sxs-lookup"><span data-stu-id="a5ac4-119">-PhoneNumber</span></span>
<span data-ttu-id="a5ac4-120">Задает номер телефона администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="a5ac4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5ac4-121">-Confirm</span></span>
<span data-ttu-id="a5ac4-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ac4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ac4-123">-WhatIf</span></span>
<span data-ttu-id="a5ac4-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5ac4-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ac4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ac4-126">CommonParameters</span></span>
<span data-ttu-id="a5ac4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5ac4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ac4-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5ac4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ac4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5ac4-129">INPUTS</span></span>

### <span data-ttu-id="a5ac4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a5ac4-130">System.String</span></span>

## <span data-ttu-id="a5ac4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5ac4-131">OUTPUTS</span></span>

### <span data-ttu-id="a5ac4-132">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="a5ac4-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="a5ac4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5ac4-133">NOTES</span></span>

## <span data-ttu-id="a5ac4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5ac4-134">RELATED LINKS</span></span>

[<span data-ttu-id="a5ac4-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="a5ac4-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

