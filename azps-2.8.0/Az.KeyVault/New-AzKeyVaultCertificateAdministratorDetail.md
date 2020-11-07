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
ms.locfileid: "93720654"
---
# <span data-ttu-id="64718-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="64718-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="64718-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64718-102">SYNOPSIS</span></span>
<span data-ttu-id="64718-103">Создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="64718-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="64718-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64718-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64718-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64718-105">DESCRIPTION</span></span>
<span data-ttu-id="64718-106">Командлет **New-AzKeyVaultCertificateAdministratorDetail** создает объект подробных данных администратора сертификата в памяти.</span><span class="sxs-lookup"><span data-stu-id="64718-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="64718-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64718-107">EXAMPLES</span></span>

### <span data-ttu-id="64718-108">Пример 1: создание объекта сведений для администратора сертификата</span><span class="sxs-lookup"><span data-stu-id="64718-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="64718-109">Эта команда создает объект сведений администратора сертификата в памяти и сохраняет его в переменной $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="64718-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="64718-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64718-110">PARAMETERS</span></span>

### <span data-ttu-id="64718-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64718-111">-DefaultProfile</span></span>
<span data-ttu-id="64718-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="64718-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64718-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="64718-113">-EmailAddress</span></span>
<span data-ttu-id="64718-114">Указывает адрес электронной почты для администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="64718-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="64718-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="64718-115">-FirstName</span></span>
<span data-ttu-id="64718-116">Задает имя администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="64718-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="64718-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="64718-117">-LastName</span></span>
<span data-ttu-id="64718-118">Задает фамилию администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="64718-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="64718-119">-Заданный</span><span class="sxs-lookup"><span data-stu-id="64718-119">-PhoneNumber</span></span>
<span data-ttu-id="64718-120">Задает номер телефона администратора сертификата.</span><span class="sxs-lookup"><span data-stu-id="64718-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="64718-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64718-121">-Confirm</span></span>
<span data-ttu-id="64718-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64718-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64718-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64718-123">-WhatIf</span></span>
<span data-ttu-id="64718-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64718-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64718-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64718-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64718-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64718-126">CommonParameters</span></span>
<span data-ttu-id="64718-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64718-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64718-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64718-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64718-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64718-129">INPUTS</span></span>

### <span data-ttu-id="64718-130">System. String</span><span class="sxs-lookup"><span data-stu-id="64718-130">System.String</span></span>

## <span data-ttu-id="64718-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64718-131">OUTPUTS</span></span>

### <span data-ttu-id="64718-132">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="64718-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="64718-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="64718-133">NOTES</span></span>

## <span data-ttu-id="64718-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64718-134">RELATED LINKS</span></span>

[<span data-ttu-id="64718-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="64718-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

